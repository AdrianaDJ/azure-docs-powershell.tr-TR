---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Import-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Import-AzureRmContext.md
ms.openlocfilehash: bb1f34a27d9f1ad5d8e851cd280751c25ebf25c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590678"
---
# <span data-ttu-id="357ed-101">Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="357ed-101">Import-AzureRmContext</span></span>

## <span data-ttu-id="357ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="357ed-102">SYNOPSIS</span></span>
<span data-ttu-id="357ed-103">Azure kimlik doğrulama bilgilerini dosyadan yükler.</span><span class="sxs-lookup"><span data-stu-id="357ed-103">Loads Azure authentication information from a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="357ed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="357ed-104">SYNTAX</span></span>

### <span data-ttu-id="357ed-105">ProfileFromDisk (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="357ed-105">ProfileFromDisk (Default)</span></span>
```
Import-AzureRmContext [-Path] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="357ed-106">Inmemoryprofile</span><span class="sxs-lookup"><span data-stu-id="357ed-106">InMemoryProfile</span></span>
```
Import-AzureRmContext [-AzureContext] <AzureRmProfile> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="357ed-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="357ed-107">DESCRIPTION</span></span>
<span data-ttu-id="357ed-108">Import-AzureRmContext cmdlet, Azure ortamı ve bağlamını ayarlamak için bir dosyadan kimlik doğrulama bilgilerini yükler.</span><span class="sxs-lookup"><span data-stu-id="357ed-108">The Import-AzureRmContext cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="357ed-109">Geçerli oturumda çalıştırdığınız cmdlet 'ler, Azure Resource Manager 'daki isteklerin kimlik doğrulaması için bu bilgileri kullanır.</span><span class="sxs-lookup"><span data-stu-id="357ed-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="357ed-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="357ed-110">EXAMPLES</span></span>

### <span data-ttu-id="357ed-111">Örnek 1: AzureRmProfile bir bağlam Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="357ed-111">Example 1: Importing a context from a AzureRmProfile</span></span>
```
PS C:\> Import-AzureRmContext -AzureContext (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="357ed-112">Bu örnek, cmdlet 'e geçirilen PSAzureProfile 'daki bir bağlamı içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="357ed-112">This example imports a context from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="357ed-113">Örnek 2: JSON dosyasındaki bağlamı Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="357ed-113">Example 2: Importing a context from a JSON file</span></span>
```
PS C:\> Import-AzureRmContext -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="357ed-114">Bu örnek, cmdlet 'e geçirilen JSON dosyasından bir bağlam seçer.</span><span class="sxs-lookup"><span data-stu-id="357ed-114">This example selects a context from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="357ed-115">Bu JSON dosyası Save-AzureRmContext 'den oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="357ed-115">This JSON file can be created from Save-AzureRmContext.</span></span>

## <span data-ttu-id="357ed-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="357ed-116">PARAMETERS</span></span>

### <span data-ttu-id="357ed-117">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="357ed-117">-AzureContext</span></span>
<span data-ttu-id="357ed-118">Bu cmdlet 'in okuduğu Azure bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="357ed-118">Specifies the Azure context from which this cmdlet reads.</span></span> <span data-ttu-id="357ed-119">Bağlam belirtmezseniz, bu cmdlet yerel varsayılan içerikten okur.</span><span class="sxs-lookup"><span data-stu-id="357ed-119">If you do not specify a context, this cmdlet reads from the local default context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Models.AzureRmProfile
Parameter Sets: InMemoryProfile
Aliases: Profile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="357ed-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="357ed-120">-DefaultProfile</span></span>
<span data-ttu-id="357ed-121">Azure ile iletişim için kullanılan kimlik bilgileri, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="357ed-121">The credentials, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="357ed-122">-Yol</span><span class="sxs-lookup"><span data-stu-id="357ed-122">-Path</span></span>
<span data-ttu-id="357ed-123">Save-AzureRMContext kullanılarak kaydedilen bağlam bilgilerinin yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="357ed-123">Specifies the path to context information saved by using Save-AzureRMContext.</span></span>

```yaml
Type: System.String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="357ed-124">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="357ed-124">-Scope</span></span>
<span data-ttu-id="357ed-125">Değişikliklerin kapsamını, örneğin değişikliklerin yalnızca geçerli işleme veya bu kullanıcı tarafından başlatılan tüm oturumlara uygulanmasını belirler.</span><span class="sxs-lookup"><span data-stu-id="357ed-125">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="357ed-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="357ed-126">-Confirm</span></span>
<span data-ttu-id="357ed-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="357ed-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="357ed-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="357ed-128">-WhatIf</span></span>
<span data-ttu-id="357ed-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="357ed-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="357ed-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="357ed-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="357ed-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="357ed-131">CommonParameters</span></span>
<span data-ttu-id="357ed-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="357ed-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="357ed-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="357ed-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="357ed-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="357ed-134">INPUTS</span></span>

### <span data-ttu-id="357ed-135">Microsoft. Azure. Commands. Common. Authentication. modeller. AzureRMProfile</span><span class="sxs-lookup"><span data-stu-id="357ed-135">Microsoft.Azure.Commands.Common.Authentication.Models.AzureRMProfile</span></span>
<span data-ttu-id="357ed-136">Azure ile iletişim kurmak için kullanılan kimlik bilgileri, hesaplar ve abonelikler kümesini içerir.</span><span class="sxs-lookup"><span data-stu-id="357ed-136">Contains the set of credentials, accounts, and subscriptions that are used to communicate with Azure.</span></span>

## <span data-ttu-id="357ed-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="357ed-137">OUTPUTS</span></span>

### <span data-ttu-id="357ed-138">Microsoft. Azure. Commands. Profile. modeller. PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="357ed-138">Microsoft.Azure.Commands.Profile.Models.PSAzureProfile</span></span>
<span data-ttu-id="357ed-139">Azure ile iletişim kurmak için kullanılabilecek kimlik bilgileri, hesaplar ve abonelikler kümesini içerir.</span><span class="sxs-lookup"><span data-stu-id="357ed-139">Contains the set of credentials, accounts, and subscriptions that can be used to communicate with Azure.</span></span>

## <span data-ttu-id="357ed-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="357ed-140">NOTES</span></span>

## <span data-ttu-id="357ed-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="357ed-141">RELATED LINKS</span></span>

