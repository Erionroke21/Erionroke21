//Membuat Multi Tab Video Streaming Responsive di Blog

var myApp=angular.module('tabs',[]);
myApp.controller('shift_tabs',function(){
  this.activeTab;
  this.makeShift=function(e){
    this.activeTab=e;
  }
  this.isActive=function(f){
    if(f==this.activeTab){
      return true
    }
  }
});

// Tab-Server movie

$(document).ready(function(){
    $("ul#tabs li").click(function(e){
        if (!$(this).hasClass("active")) {
            var tabNum = $(this).index();
            var nthChild = tabNum+1;
            $("ul#tabs li.active").removeClass("active");
            $(this).addClass("active");
            $("ul#tab li.active").removeClass("active");
            $("ul#tab li:nth-child("+nthChild+")").addClass("active");
        }
    });
});
