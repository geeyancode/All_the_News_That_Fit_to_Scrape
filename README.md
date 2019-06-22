Part 1 (Connection)
    Step 1 Create and test localhost port
        <!-- // 
    var port = process.env.PORT || 3000;
    app.listen(port, function() {
    console.log("Listening on PORT " + port);
    }); -->
    Step 2 Setup connection to MongoDB
    <!-- /
    mongoose.connect("mongodb://localhost/scraped_news");
    // const MONGODB_URI =
    //   process.env.MONGODB_URI || "mongodb://localhost/scraper_news";
    // mongoose.connect(MONGODB_URI, { useNewUrlParser: true }); -->

    Step 3 start mongod
    Step 4 test connection to mongo server

Part 2 (Models)
    Step 1 create/setup models
        a. articlemodel 
            create schema for articlemodel
            

                    <!-- 
                        var mongoose = require("mongoose");
                        var Schema = mongoose.Schema;
                    var ArticleSchema = new Schema({
                    title: {
                        type: String,
                        required: true
                    },
                    link: {
                        type: String,
                        required: true
                    },
                    comment: [
                        {
                        type: Schema.Types.ObjectId,
                        ref: "Comment"
                        }
                    ]
                    });
                    var Article = mongoose.model("Article", ArticleSchema);
                    module.exports = Article; -->
        b. commentmodel
            create schema for commentmodel
                    <!-- var mongoose = require("mongoose");

                    var Schema = mongoose.Schema;
                    
                    var CommentSchema = new Schema({
                    name: {
                        type: String
                    },
                    body: {
                        type: String,
                        required: true
                    }
                    });
                    var Comment = mongoose.model("Comment", CommentSchema);
                    module.exports = Comment; -->

Part 3 (Handlebars)frontend
    views-folder
        a.indexHandlebars-file
        b.--articleHandlerbars-file
        c.partialsfolder
            1.navfolder
                navbar-file(branding area)
            2.footer-file
        d.layouts-folder
            1.main.Handlebars(head, html, scripts.)
            
Part 4 Controller - This part is not fully working yet
        a.connection to models
        b.setup routes
