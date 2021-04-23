# Timeout-Popup
Make a Time Out Popup using Jquery

######Include Bootstrap CSS library  in the header:

```
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">
```

######then Include Jquery, Bootstrap, Cookie library  in the footer:

```
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery-cookie/1.4.1/jquery.cookie.min.js"></script>
```

######Now Add Bootstrap Modal in The Body:

```
<div class="modal fade" id="exampleModal" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel"
     aria-hidden="true">
    <div class="modal-dialog" role="document">
        <div class="modal-content">
            <div class="modal-header">
                <h5 class="modal-title" id="exampleModalLabel">Modal title</h5>
                <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                    <span aria-hidden="true">&times;</span>
                </button>
            </div>
            <div class="modal-body">
                Lorem ipsum dolor sit amet, consectetur adipisicing elit. Consequatur consequuntur eligendi fuga
                inventore rem reprehenderit sapiente velit! Adipisci aperiam atque explicabo harum ipsam libero pariatur
                perferendis, quod reprehenderit, saepe, sunt.
            </div>

        </div>
    </div>
</div>
```

######Here is the main part add Jquery For timeout popup:

```
<script>
    $(document).ready(function () {
        // if there is no cookie
        if ($.cookie('show_modal') == null) {


            $('#exampleModal').modal('show');
            $.cookie('show_modal', 'yes', {expires: 1});
            // set cookie expiry  1 day

        } else { // have cookie
            // do something
        }
    });
</script>
```

Codepen link : https://codepen.io/saif175/pen/PoWXVaX