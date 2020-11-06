---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContext.md
ms.openlocfilehash: 3ad029e84245aee45bbcdd08ea0d78c5e57b985e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590683"
---
# <span data-ttu-id="32ddb-101">Get-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="32ddb-101">Get-AzureRmContext</span></span>

## <span data-ttu-id="32ddb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32ddb-102">SYNOPSIS</span></span>
<span data-ttu-id="32ddb-103">Azure Resource Manager isteklerinin kimlik doğrulaması için kullanılan meta verileri alır.</span><span class="sxs-lookup"><span data-stu-id="32ddb-103">Gets the metadata used to authenticate Azure Resource Manager requests.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32ddb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="32ddb-104">SYNTAX</span></span>

### <span data-ttu-id="32ddb-105">GetSingleContext (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="32ddb-105">GetSingleContext (Default)</span></span>
```
Get-AzureRmContext [-DefaultProfile <IAzureContextContainer>] [[-Name] <String>] [<CommonParameters>]
```

### <span data-ttu-id="32ddb-106">Listallbağlamları</span><span class="sxs-lookup"><span data-stu-id="32ddb-106">ListAllContexts</span></span>
```
Get-AzureRmContext [-ListAvailable] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32ddb-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="32ddb-107">DESCRIPTION</span></span>
<span data-ttu-id="32ddb-108">Get-AzureRmContext cmdlet 'i, Azure Resource Manager isteklerinin kimlik doğrulaması için kullanılan geçerli meta verileri alır.</span><span class="sxs-lookup"><span data-stu-id="32ddb-108">The Get-AzureRmContext cmdlet gets the current metadata used to authenticate Azure Resource Manager requests.</span></span>

<span data-ttu-id="32ddb-109">Bu cmdlet Active Directory hesabını, Active Directory kiracısı, Azure aboneliğini ve hedeflenen Azure ortamını alır.</span><span class="sxs-lookup"><span data-stu-id="32ddb-109">This cmdlet gets the Active Directory account, Active Directory tenant, Azure subscription, and the targeted Azure environment.</span></span>
<span data-ttu-id="32ddb-110">Azure Resource Manager cmdlet 'leri Azure Resource Manager istekleri yaparken varsayılan olarak bu ayarları kullanın.</span><span class="sxs-lookup"><span data-stu-id="32ddb-110">Azure Resource Manager cmdlets use these settings by default when making Azure Resource Manager requests.</span></span>

## <span data-ttu-id="32ddb-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="32ddb-111">EXAMPLES</span></span>

### <span data-ttu-id="32ddb-112">Örnek 1: geçerli bağlamı alma</span><span class="sxs-lookup"><span data-stu-id="32ddb-112">Example 1: Getting the current context</span></span>
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

<span data-ttu-id="32ddb-113">Bu örnekte, Add-AzureRmAccount kullanarak bir Azure aboneliğiyle hesabınıza oturum açıyoruz ve ardından Get-AzureRmContext ' i çağırarak geçerli oturumun bağlamını alıyoruz.</span><span class="sxs-lookup"><span data-stu-id="32ddb-113">In this example we are logging into our account with an Azure subscription using Add-AzureRmAccount, and then we are getting the context of the current session by calling Get-AzureRmContext.</span></span>

### <span data-ttu-id="32ddb-114">Örnek 2: kullanılabilir tüm bağlamların listelenmesi</span><span class="sxs-lookup"><span data-stu-id="32ddb-114">Example 2: Listing all available contexts</span></span>
```
PS C:\> Get-AzureRmContext -ListAvailable

Name                  : Test
Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :

Name                  : Production
Environment           : AzureCloud
Account               : prod@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Production Subscription
CurrentStorageAccount :
```

<span data-ttu-id="32ddb-115">Bu örnekte, kullanılabilen tüm içerikler görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="32ddb-115">In this example, all currently available contexts are displayed.</span></span>  <span data-ttu-id="32ddb-116">Kullanıcı, select-AzureRmContext kullanarak bu bağlamların birini seçebilir.</span><span class="sxs-lookup"><span data-stu-id="32ddb-116">The user may select one of these contexts using Select-AzureRmContext.</span></span>

## <span data-ttu-id="32ddb-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="32ddb-117">PARAMETERS</span></span>

### <span data-ttu-id="32ddb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32ddb-118">-DefaultProfile</span></span>
<span data-ttu-id="32ddb-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="32ddb-119">The credentials, account, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32ddb-120">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="32ddb-120">-ListAvailable</span></span>
<span data-ttu-id="32ddb-121">Geçerli oturumdaki kullanılabilir tüm içeriği listeler.</span><span class="sxs-lookup"><span data-stu-id="32ddb-121">List all available contexts in the current session.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAllContexts
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32ddb-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="32ddb-122">-Name</span></span>
<span data-ttu-id="32ddb-123">İçeriğin adı</span><span class="sxs-lookup"><span data-stu-id="32ddb-123">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: GetSingleContext
Aliases: 
Accepted values: [contrib@AzureSDKTeam.onmicrosoft.com, 0b1f6471-1bf0-4dda-aec3-cb9272f09590], [markcowl@microsoft.com, 00977cdb-163f-435f-9c32-39ec8ae61f4d]

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32ddb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32ddb-124">CommonParameters</span></span>
<span data-ttu-id="32ddb-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="32ddb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32ddb-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32ddb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32ddb-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="32ddb-127">INPUTS</span></span>

## <span data-ttu-id="32ddb-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="32ddb-128">OUTPUTS</span></span>

### <span data-ttu-id="32ddb-129">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="32ddb-129">PSAzureContext</span></span>
<span data-ttu-id="32ddb-130">Bu cmdlet, Azure Resource Manager cmdlet 'lerinin kullandığı hesap, kiracı ve aboneliği döndürür.</span><span class="sxs-lookup"><span data-stu-id="32ddb-130">This cmdlet returns the account, tenant, and subscription used by Azure Resource Manager cmdlets.</span></span>

## <span data-ttu-id="32ddb-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="32ddb-131">NOTES</span></span>

## <span data-ttu-id="32ddb-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="32ddb-132">RELATED LINKS</span></span>

[<span data-ttu-id="32ddb-133">Set-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="32ddb-133">Set-AzureRMContext</span></span>](./Set-AzureRMContext.md)

