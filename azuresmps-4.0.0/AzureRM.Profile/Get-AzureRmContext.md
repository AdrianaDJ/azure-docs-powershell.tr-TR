---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 914b75e3952f7841aaf3ff505f51f7b4ebdc6044
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571750"
---
# <span data-ttu-id="df864-101">Get-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="df864-101">Get-AzureRmContext</span></span>

## <span data-ttu-id="df864-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df864-102">SYNOPSIS</span></span>
<span data-ttu-id="df864-103">Azure Resource Manager isteklerinin kimlik doğrulaması için kullanılan meta verileri alır.</span><span class="sxs-lookup"><span data-stu-id="df864-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

## <span data-ttu-id="df864-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="df864-104">SYNTAX</span></span>

```
Get-AzureRmContext [<CommonParameters>]
```

## <span data-ttu-id="df864-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="df864-105">DESCRIPTION</span></span>
<span data-ttu-id="df864-106">Get-AzureRmContext cmdlet 'i, Azure Resource Manager isteklerinin kimlik doğrulaması için kullanılan geçerli meta verileri alır.</span><span class="sxs-lookup"><span data-stu-id="df864-106">The Get-AzureRmContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>

<span data-ttu-id="df864-107">Bu cmdlet Active Directory hesabını, Active Directory kiracısı, Azure aboneliğini ve hedeflenen Azure ortamını alır.</span><span class="sxs-lookup"><span data-stu-id="df864-107">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="df864-108">Azure Resource Manager cmdlet 'leri Azure Resource Manager istekleri yaparken varsayılan olarak bu ayarları kullanın.</span><span class="sxs-lookup"><span data-stu-id="df864-108">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="df864-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="df864-109">EXAMPLES</span></span>

### <span data-ttu-id="df864-110">Örnek 1: geçerli bağlamı alma</span><span class="sxs-lookup"><span data-stu-id="df864-110">Example 1: Getting the current context</span></span>
```
PS C:\> Add-AzureRmAccount
PS C:\> Get-AzureRmContext

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="df864-111">Bu örnekte, Add-AzureRmAccount kullanarak bir Azure aboneliğiyle hesabınıza oturum açıyoruz ve ardından Get-AzureRmContext ' i çağırarak geçerli oturumun bağlamını alıyoruz.</span><span class="sxs-lookup"><span data-stu-id="df864-111">In this example we are logging into our account with an Azure subscription using Add-AzureRmAccount, and then we are getting the context of the current session by calling Get-AzureRmContext.</span></span>

## <span data-ttu-id="df864-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="df864-112">PARAMETERS</span></span>

### <span data-ttu-id="df864-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df864-113">CommonParameters</span></span>
<span data-ttu-id="df864-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="df864-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df864-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df864-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df864-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="df864-116">INPUTS</span></span>

## <span data-ttu-id="df864-117">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="df864-117">OUTPUTS</span></span>

### <span data-ttu-id="df864-118">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="df864-118">PSAzureContext</span></span>
<span data-ttu-id="df864-119">Bu cmdlet, Azure Resource Manager cmdlet 'lerinin kullandığı hesap, kiracı ve aboneliği döndürür.</span><span class="sxs-lookup"><span data-stu-id="df864-119">This cmdlet returns the account, tenant, and subscription used by Azure Resource Manager cmdlets.</span></span>

## <span data-ttu-id="df864-120">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="df864-120">NOTES</span></span>

## <span data-ttu-id="df864-121">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="df864-121">RELATED LINKS</span></span>

[<span data-ttu-id="df864-122">Set-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="df864-122">Set-AzureRMContext</span></span>]()

