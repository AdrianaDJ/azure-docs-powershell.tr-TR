---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/test-azappconfigurationstorenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Test-AzAppConfigurationStoreNameAvailability.md
ms.openlocfilehash: c7f315d1989a6cbbfbfa08cf3f59cff8ccd811bc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107980"
---
# <span data-ttu-id="7c677-101">Test-AzAppConfigurationStoreNameAvailability</span><span class="sxs-lookup"><span data-stu-id="7c677-101">Test-AzAppConfigurationStoreNameAvailability</span></span>

## <span data-ttu-id="7c677-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c677-102">SYNOPSIS</span></span>
<span data-ttu-id="7c677-103">Yapılandırma deposu adının kullanıma uygun olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="7c677-103">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="7c677-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7c677-104">SYNTAX</span></span>

```
Test-AzAppConfigurationStoreNameAvailability -Name <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7c677-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7c677-105">DESCRIPTION</span></span>
<span data-ttu-id="7c677-106">Yapılandırma deposu adının kullanıma uygun olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="7c677-106">Checks whether the configuration store name is available for use.</span></span>

## <span data-ttu-id="7c677-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7c677-107">EXAMPLES</span></span>

### <span data-ttu-id="7c677-108">Örnek 1: uygulama yapılandırma deposu adının test kullanılabilirliği</span><span class="sxs-lookup"><span data-stu-id="7c677-108">Example 1: Test availability of the app configuration store name</span></span>

```powershell
PS C:\> Test-AzAppConfigurationStoreNameAvailability -Name appconfig-test01

Message                               NameAvailable Reason
-------                               ------------- ------
The specified name is already in use. False         AlreadyExists
```

<span data-ttu-id="7c677-109">Bu komut, uygulama yapılandırma deposu adının kullanılabilirliğini sınar.</span><span class="sxs-lookup"><span data-stu-id="7c677-109">This command tests availability of the app configuration store name.</span></span>

## <span data-ttu-id="7c677-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7c677-110">PARAMETERS</span></span>

### <span data-ttu-id="7c677-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c677-111">-DefaultProfile</span></span>
<span data-ttu-id="7c677-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7c677-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c677-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="7c677-113">-Name</span></span>
<span data-ttu-id="7c677-114">Uygunluk adı.</span><span class="sxs-lookup"><span data-stu-id="7c677-114">The name to check for availability.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c677-115">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="7c677-115">-SubscriptionId</span></span>
<span data-ttu-id="7c677-116">Microsoft Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="7c677-116">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c677-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="7c677-117">-Confirm</span></span>
<span data-ttu-id="7c677-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7c677-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c677-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c677-119">-WhatIf</span></span>
<span data-ttu-id="7c677-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7c677-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c677-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7c677-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c677-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c677-122">CommonParameters</span></span>
<span data-ttu-id="7c677-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7c677-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c677-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7c677-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c677-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7c677-125">INPUTS</span></span>

## <span data-ttu-id="7c677-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7c677-126">OUTPUTS</span></span>

### <span data-ttu-id="7c677-127">Microsoft. Azure. PowerShell. cmdlet. AppConfiguration. modeller. Api20200601. INameAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="7c677-127">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.INameAvailabilityStatus</span></span>

## <span data-ttu-id="7c677-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7c677-128">NOTES</span></span>

<span data-ttu-id="7c677-129">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="7c677-129">ALIASES</span></span>

## <span data-ttu-id="7c677-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7c677-130">RELATED LINKS</span></span>

