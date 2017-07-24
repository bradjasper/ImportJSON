(function($){
  $.fn.extend( {
		share_is_email: function( value ) {
	    return /^((([a-z]|\d|[!#\$%&'\*\+\-\/=\?\^_`{\|}~]|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])+(\.([a-z]|\d|[!#\$%&'\*\+\-\/=\?\^_`{\|}~]|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])+)*)|((\x22)((((\x20|\x09)*(\x0d\x0a))?(\x20|\x09)+)?(([\x01-\x08\x0b\x0c\x0e-\x1f\x7f]|\x21|[\x23-\x5b]|[\x5d-\x7e]|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])|(\\([\x01-\x09\x0b\x0c\x0d-\x7f]|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF]))))*(((\x20|\x09)*(\x0d\x0a))?(\x20|\x09)+)?(\x22)))@((([a-z]|\d|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])|(([a-z]|\d|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])([a-z]|\d|-|\.|_|~|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])*([a-z]|\d|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])))\.)+(([a-z]|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])|(([a-z]|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])([a-z]|\d|-|\.|_|~|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])*([a-z]|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])))\.?$/i.test( this.val() );
		}
  } );
  
	$( document ).ready(function() {
		$( '.sharing a.sharing-anchor' ).click( function() {
			return false;
		} );

		$( '.sharing a' ).each( function() {
			if ( $( this ).attr( 'href' ) && $( this ).attr( 'href' ).indexOf( 'share=' ) != -1 )
				$( this ).attr( 'href', $( this ).attr( 'href' ) + '&nb=1' );
		} );
		
		// Show hidden buttons
		$( '.sharing a.sharing-anchor' ).hover( function() {
			if ( $( this ).data( 'hasappeared' ) !== true ) {
				var item     = $( this ).parents( 'div:first' ).find( '.inner' );
				var original = $( this );
				
				// Create a timer to make the area appear if the mouse hovers for a period
				var timer = setTimeout( function() {
					$( '#sharing_email' ).slideUp( 200 );

					$( item ).css( {
						left: $( original ).position().left + 'px',
						top: $( original ).position().top + $( original ).height() + 3 + 'px'
					} ).slideDown( 200, function() {
						// Mark the item as have being appeared by the hover
						$( original ).data( 'hasappeared', true ).data( 'hasoriginal', true ).data( 'hasitem', false );
						
						// Remove all special handlers
						$( item ).mouseleave( handler_item_leave ).mouseenter( handler_item_enter );
						$( original ).mouseleave( handler_original_leave ).mouseenter( handler_original_enter );
						
						// Add a special handler to quickly close the item
						$( original ).click( close_it );
					} );
					
					// The following handlers take care of the mouseenter/mouseleave for the share button and the share area - if both are left then we close the share area
					var handler_item_leave = function() {
						$( original ).data( 'hasitem', false );
						
						if ( $( original ).data( 'hasoriginal' ) === false ) {
							var timer = setTimeout( close_it, 800 );
							$( original ).data( 'timer2', timer );
						}
					};

					var handler_item_enter = function() {
						$( original ).data( 'hasitem', true );
						clearTimeout( $( original ).data( 'timer2' ) );
					} 
					
					var handler_original_leave = function() {
						$( original ).data( 'hasoriginal', false );
						
						if ( $( original ).data( 'hasitem' ) === false ) {
							var timer = setTimeout( close_it, 800 );
							$( original ).data( 'timer2', timer );
						}
					};
					
					var handler_original_enter = function() {
						$( original ).data( 'hasoriginal', true );
						clearTimeout( $( original ).data( 'timer2' ) );
					};
	
					var close_it = function() {
						item.slideUp( 200 );

						// Clear all hooks
						$( original ).unbind( 'mouseleave', handler_original_leave ).unbind( 'mouseenter', handler_original_enter );
						$( item ).unbind( 'mouseleave', handler_item_leave ).unbind( 'mouseenter', handler_item_leave );
						$( original ).data( 'hasappeared', false );
						$( original ).unbind( 'click', close_it );
						return false;
					};
				}, 200 );
				
				// Remember the timer so we can detect it on the mouseout
				$( this ).data( 'timer', timer );
			}
		}, function() {
			// Mouse out - remove any timer
			clearTimeout( $( this ).data( 'timer' ) );
			$( this ).data( 'timer', false );
		} );
		
		// Add click functionality
		$( '.sharing ul' ).each( function( item ) {
			printUrl = function ( uniqueId, urlToPrint ) {
				$( 'body:first' ).append( '<iframe style="position:fixed;top:100;left:100;height:1px;width:1px;border:none;" id="printFrame-' + uniqueId + '" name="printFrame-' + uniqueId + '" src="' + urlToPrint + '" onload="frames[\'printFrame-' + uniqueId + '\'].focus();frames[\'printFrame-' + uniqueId + '\'].print();"></iframe>' )
			};
			
			// Print button
			$( this ).find( '.share-print a' ).click( function() {
				ref = $( this ).attr( 'href' );
				
				var do_print = function() {
					if ( ref.indexOf( '#print' ) == -1 ) {
						uid = new Date().getTime();
						printUrl( uid , ref );
					}
					else
						print();
				}
				
				// Is the button in a dropdown?
				if ( $( this ).parents( '.sharing-hidden' ).length > 0 ) {
					$( this ).parents( '.inner' ).slideUp( 0, function() {
						do_print();
					} );
				}
				else
					do_print();

				return false;
			} );
			
			// Press This button
			$( this ).find( '.share-press-this a' ).click( function() {
			 	var s = '';
			 	
			  if ( window.getSelection )
			    s = window.getSelection();
			  else if( document.getSelection )
			    s = document.getSelection();
			  else if( document.selection )
			    s = document.selection.createRange().text;

				if ( s )
					$( this ).attr( 'href', $( this ).attr( 'href' ) + '&sel=' + encodeURI( s ) );

				if ( !window.open( $( this ).attr( 'href' ), 't', 'toolbar=0,resizable=1,scrollbars=1,status=1,width=720,height=570' ) ) 
					document.location.href = $( this ).attr( 'href' );

				return false;
			} );

			// Email button
			$( this ).find( '.share-email a' ).click( function() {
				var url = $( this ).attr( 'href' );
				
				if ( $( '#sharing_email' ).is( ':visible' ) )
					$( '#sharing_email' ).slideUp( 200 );
				else {
					$( '.sharing .inner' ).slideUp();

					$( '#sharing_email .response' ).remove();
					$( '#sharing_email form' ).show();
					$( '#sharing_email form input[type=submit]' ).removeAttr( 'disabled' );
					$( '#sharing_email form a.sharing_cancel' ).show();

					// Show dialog
					$( '#sharing_email' ).css( {
						left: $( this ).offset().left + 'px',
						top: $( this ).offset().top + $( this ).height() + 'px'
					} ).slideDown( 200 );
					
					// Hook up other buttons
					$( '#sharing_email a.sharing_cancel' ).unbind( 'click' ).click( function() {
						$( '#sharing_email .errors' ).hide();
						$( '#sharing_email' ).slideUp( 200 );
						$( '#sharing_background' ).fadeOut();
						return false;
					} );
					
					// Submit validation
					$( '#sharing_email input[type=submit]' ).unbind( 'click' ).click( function() {
						var form = $( this ).parents( 'form' );
						
						// Disable buttons + enable loading icon
						$( this ).attr( 'disabled', 'disabled' );
						form.find( 'a.sharing_cancel' ).hide();
						form.find( 'img.loading' ).show();
						
						$( '#sharing_email .errors' ).hide();
						$( '#sharing_email .error' ).removeClass( 'error' );
						
						if ( $( '#sharing_email input[name=source_email]' ).share_is_email() == false )
							$( '#sharing_email input[name=source_email]' ).addClass( 'error' );
							
						if ( $( '#sharing_email input[name=target_email]' ).share_is_email() == false )
							$( '#sharing_email input[name=target_email]' ).addClass( 'error' );
						
						if ( $( '#sharing_email .error' ).length == 0 ) {
							// AJAX send the form
							$.ajax( {
								url: url,
								type: 'POST',
								data: form.serialize(),
								success: function( response ) {
									form.find( 'img.loading' ).hide();

									if ( response == '1' || response == '2' || response == '3' ) {
										$( '#sharing_email .errors-' + response ).show();
										form.find( 'input[type=submit]' ).removeAttr( 'disabled' );
										form.find( 'a.sharing_cancel' ).show();
									}
									else {
										$( '#sharing_email form' ).hide();
										$( '#sharing_email' ).append( response );
										$( '#sharing_email a.sharing_cancel' ).click( function() {
											$( '#sharing_email' ).slideUp( 200 );
											$( '#sharing_background' ).fadeOut();
											return false;
										} );
									}
								}
							} );
							
							return false;
						}
						
						form.find( 'img.loading' ).hide();
						form.find( 'input[type=submit]' ).removeAttr( 'disabled' );
						form.find( 'a.sharing_cancel' ).show();
						$( '#sharing_email .errors-1' ).show();

						return false;
					} );
				}
				
				return false;
			} );
		} );
		
		$( 'li.share-email, li.share-custom a.sharing-anchor' ).addClass( 'share-service-visible' );
	} );
})( jQuery );
