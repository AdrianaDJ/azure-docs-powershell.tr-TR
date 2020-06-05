---
title: Azure PowerShell ile Azure aboneliklerini yönetme
description: Azure PowerShell ile Azure aboneliklerini yönetme
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/04/2019
ms.openlocfilehash: 4947435259f78c10e4f67434eb62ec8d4c3c6013
ms.sourcegitcommit: cef87acc9f2a0d296bef74f526afd2e067e8146b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/02/2020
ms.locfileid: "84299188"
---
# <a name="use-multiple-azure-subscriptions"></a>Birden çok Azure aboneliği kullanma

Çoğu Azure kullanıcısı sadece tek bir aboneliğe sahip olur. Ancak, birden çok kuruluşun parçasıysanız veya kuruluşunuz belirli kaynaklara erişimi gruplar arasında böldüyse, Azure’da birden fazla aboneliğiniz olabilir. CLI hem genel olarak hem de komut başına abonelik seçimini destekler.

Abonelikler, faturalama ve maliyet yönetimi hakkında ayrıntılı bilgi için, [faturalama ve maliyet yönetimi belgelerine](/azure/billing/) bakın.

## <a name="tenants-users-and-subscriptions"></a>Kiracılar, kullanıcılar ve abonelikler

Azure’da kiracılar, kullanıcılar ve abonelikler arasındaki fark biraz kafa karıştırıcı olabilir. _Kiracı_, kuruluşun tamamını kapsayan bir Azure Active Directory varlığıdır. Bu kiracı en az bir _abonelik_ ve _kullanıcıya_ sahiptir. Kullanıcı bir kişidir ve yalnızca ait olduğu kuruluş olan tek bir kiracı ile ilişkilidir. Kullanıcılar, kaynakları oluşturmak, yönetmek ve kullanmak için Azure’da oturum açan hesaplardır.
Bir kullanıcının, Microsoft ile bulut hizmetlerini (Azure dahil) kullanmak için yapılan anlaşmaları ifade eden birden çok _aboneliğe_ erişimi olabilir. Her kaynak bir abonelik ile ilişkilidir.

Kiracılar, kullanıcılar ve abonelikler arasındaki farklar hakkında daha fazla bilgi için bkz. [Azure bulut terimleri sözlüğü](/azure/azure-glossary-cloud-terminology).  Azure Active Directory kiracınıza yeni bir abonelik ekleme hakkında bilgi almak için bkz. [Azure Active Directory kiracınızla bir Azure aboneliğini ilişkilendirme veya abonelik ekleme](/azure/active-directory/active-directory-how-subscriptions-associated-directory).
Belirli bir kiracıda oturum açmayı öğrenmek için bkz. [Azure PowerShell ile oturum açma](/powershell/azure/authenticate-azureps).

## <a name="change-the-active-subscription"></a>Etkin aboneliği değiştirme

Azure PowerShell'de, bir abonelik için kaynaklara erişirken geçerli Azure oturumunuzla ilişkilendirilmiş aboneliğin değiştirilmesi gerekir.
Bu işlem etkin oturum bağlamı, cmdlet'lerin çalıştırılacağı kiracı, abonelik ve kullanıcı hakkındaki bilgiler değiştirilerek yapılır.
Abonelikleri değiştirmek için, önce [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) ile bir Azure PowerShell Context nesnesinin alınması ve ardından [Set-AzContext](/powershell/module/az.accounts/set-azcontext) ile geçerli bağlamın değiştirilmesi gerekir.

Sonraki örnekte, etkin durumdaki kiracıda bir aboneliği alma ve bunu etkin oturum olarak ayarlama işlemleri gösterilir:

```powershell-interactive
$context = Get-AzSubscription -SubscriptionId ...
Set-AzContext $context
```

Azure PowerShell bağlamları hakkında daha fazla bilgi edinmek, bunların nasıl kaydedildiğini ve kolayca birden çok abonelikle çalışmak üzere aralarında nasıl hızla geçiş yapıldığını öğrenmek için, bkz. [Azure PowerShell bağlamlarında kimlik bilgilerini kalıcı hale getirme](context-persistence.md).
