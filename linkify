jQuery(document).ready(function() {
  function linkify(text) {
    var urlRegex = /(([a-z]+:\/\/)?(([a-z0-9\-]+\.)+([a-z]{2}|aero|arpa|biz|com|coop|edu|gov|info|int|jobs|mil|museum|name|nato|net|org|pro|travel|local|internal|in))(:[0-9]{1,5})?(\/[a-z0-9_\-\.~]+)*(\/([a-z0-9_\-\.]*)(\?[a-z0-9+_\-\.%=&amp;]*)?)?(#[a-zA-Z0-9!$&'()*+.=-_~:@\/?]*)?)(\s+|$)/gim;
    //add a space before html tags to capture more possible url's
    text = text.replace(/(<([^>]+)>)/ig, function(tag) {
      return " " + tag;
    });
    //return linkified html
    return text.replace(urlRegex, function(url) {
      return '<a target="_blank" href="' + url + '">' + url + '</a>';
    })
  }

  jQuery('.simcal-event-description').each(function(i, element) {
    element.innerHTML = linkify(element.innerHTML);
  });
});
