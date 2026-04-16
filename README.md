<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8" />
<meta name="description" content="Author: International Register of Shipping (IRS) [IS], Category: Request for quotation anonymously of Vessels, Ships, Company, Offshore">
<title>Certificate Verification</title>
<meta name="keywords" content="IRS,IS,RFQ,International Register of Shipping,Quotation,Request for Quotation,Survey,Vessel Survey,Ship Survey,Company Survey,EEXI,Calculator,EEXI Calculator">
<link rel="SHORTCUT ICON" href="/Content/favicon.ico" />
<!-- Bootstrap core CSS -->
<link href="/Content/bootstrap.min.css" rel="stylesheet">
<link href="/css/fontawesome/css/all.min.css" rel="stylesheet">


<style>
.jumbotron {
padding-top: 8rem;
color: #5D8375;
}

.row.header {
font-weight: bold;
color: #E3FFE4;
background: #5D8375;
}

.row.header.red {
background: red;
text-align: center;
}

.form-group label {
font-weight: bold;
}
</style>

<!-- Bootstrap core JavaScript
================================================== -->
<!-- Placed at the end of the document so the pages load faster -->
<script src="/Scripts/jquery-3.4.1.min.js"></script>
<script src="/Scripts/popper.js"></script>
<script src="/Scripts/bootstrap.min.js"></script>

</head>
<body style="background-color:midnightblue">
<nav class="navbar navbar-expand-md navbar-dark fixed-top" style="background-color: #B4DCE7;">
<a class="navbar-brand" href="http://www.intlreg.org" target="_blank"><img src="../../Content/app-images/INTLREG_Logo.PNG" height="90"></a>
<a class="navbar-brand" target="_blank" href="http://www.intlreg.org" style="color: midnightblue;"></a>
</nav>
<main role="main" class="container">

<body>
<div class="jumbotron">
<div style="text-align:center"><h1>Welcome to the International Register of Shipping Online Verification System</h1></div>
<form action="/CertificateVerification/VerifyCertificateNo" data-ajax="true" data-ajax-method="POST" data-ajax-mode="replace" data-ajax-update="#replace" id="form0" method="post"> <div class="container" id="replace">
<div class="row">&nbsp;</div>
<div class="form-row">
<div class="form-group col-md-4">
<label for="CertificateNo">Cert./UTN No</label>
<div class="input-group mb-3">
<input class="form-control" id="CertificateNo" name="CertificateNo" type="text" value="IRR-PACI-FT-26-00325" />
<div class="input-group-append">
<button id="search-button" type="submit" class="btn btn-success"><i class="fa fa-search"></i> Search</button>
</div>
</div>
</div>
</div>
<div class="row">&nbsp;</div>
<script>
$(document).ready(function () {
var popup = $('#certVerifyPopup'),
validity = 1;

popup.on('shown.bs.modal', function () {
if (validity == 0) {
$('#certValidationMessage').append('Expired Certificate');
$('#icon-check').addClass('fa-times');
$('.modal-body *').addClass('text-danger');


} else if (validity == 1) {
$('#certValidationMessage').append('Valid Certificate');
$('#icon-check').addClass('fa-check');
$('.modal-body *').addClass('text-success');
} else if (validity == 2) {
$('#certValidationMessage').append('Revoked Certificate');
$('#icon-check').addClass('fa-times');
$('.modal-body *').addClass('text-danger');
} else if (validity == 3) {
$('#certValidationMessage').append('Invalid due to Overdue Surveys');
$('#icon-check').addClass('fa-times');
$('.modal-body *').addClass('text-warning');
statusCss = 'text-warning'
} else if (validity == 4) {
$('#certValidationMessage').append('SUSPENDED');
$('#icon-check').addClass('fa-times');
$('.modal-body *').addClass('text-warning');
statusCss = 'text-warning'
}
});

popup.modal({
backdrop: 'static',
keyboard: false
});

popup.on('hidden.bs.modal', function () {
$(this).data('bs.modal', null);
});
});
</script>
<div class="row header">
<div class="col-sm-3 border-bottom border-right border-light">Certificate No</div>
<div class="col-sm-3 border-bottom border-right border-light">Type of Certification</div>
<div class="col-sm-3 border-bottom border-right border-light">Name of Ship/Company</div>
<div class="col-sm-1 border-bottom border-right border-light">IMO</div>
<div class="col-sm-2 border-bottom border-light">Call Sign</div>
</div>
<div class="row">
<div class="col-sm-3 border-right border-left border-dark">
IRR-PACI-FT-26-00325
</div>
<div class="col-sm-3 border-right border-dark">
[PACI] Plan Appraisal Letter - Attained Carbon Intensity Indicator (CII) (Full Term)
</div>
<div class="col-sm-3 border-right border-dark">
GAS BELLA
<br />
<br />
<div class="text-danger">
</div>
</div>
<div class="col-sm-1 border-right border-dark">
9147394
</div>
<div class="col-sm-2 border-right border-dark">
3X2139
</div>
</div>
<div class="row header">
<div class="col-sm-3 border-right border-light">Issue Date</div>
<div class="col-sm-3 border-right border-light">Expiry Date</div>
<div class="col-sm-6">Status</div>
</div>
<div class="row">
<div class="col-sm-3 border border-dark">
01-Jan-2025
</div>
<div class="col-sm-3 border border-left-0 border-dark">
</div>
<div class="col-sm-6 border border-left-0 border-dark ">

Issued. Active Certificate No is IRR-PACI-FT-26-00325
</div>
</div>
<div class="datarow">&nbsp;</div>
<div class="row header">
<div class="col-sm-1 border-right border-light">#</div>
<div class="col-sm-6 border-right border-light">Survey</div>
<div class="col-sm-2 border-right border-light">Type</div>
<div class="col-sm-3">Status</div>
</div>
<div class="row">
<div class="col-sm-1 border border-dark">1</div>
<div class="col-sm-6 border border-left-0 border-dark">
Plan Appraisal Of Attained Carbon Intensity Indicator (CII)
</div>
<div class="col-sm-2 border border-left-0 border-dark">Approval</div>
<div class="col-sm-3 border border-left-0 border-dark">12-Jan-2026</div>
</div>
</div>
</form> </div>

<!-- The Modal -->
<div class="modal" id="certVerifyPopup">
<div class="modal-dialog modal-dialog-centered modal-sm">
<div class="modal-content">

<!-- Modal body -->
<div class="modal-body text-center">
<i id="icon-check" class="fa fa-4x"></i>
<br />
<br />
<h2 id="certValidationMessage"></h2>
<br />
<h6>Please verify the information</h6>
</div>

<!-- Modal footer -->
<div class="modal-footer">
<div class="col-sm-12 text-center">
<button type="button" class="btn btn-success " data-dismiss="modal">Ok</button>
</div>
</div>

</div>
</div>
</div>
</body>

</main>


</body>
</html>
