---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveApplicationControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControl.md
ms.openlocfilehash: cc86d7262270a253c9e77f0aec923c2a9fad693a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324271"
---
# <span data-ttu-id="9818f-101">Get-AzSecurityAdaptiveApplicationControl</span><span class="sxs-lookup"><span data-stu-id="9818f-101">Get-AzSecurityAdaptiveApplicationControl</span></span>

## <span data-ttu-id="9818f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9818f-102">SYNOPSIS</span></span>
<span data-ttu-id="9818f-103">Abonelik için uygulama denetimi VM/sunucu gruplarının bir listesini alır.</span><span class="sxs-lookup"><span data-stu-id="9818f-103">Gets a list of application control VM/server groups for the subscription.</span></span>

## <span data-ttu-id="9818f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9818f-104">SYNTAX</span></span>

### <span data-ttu-id="9818f-105">SubscriptionScope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9818f-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAdaptiveApplicationControl [-SubscriptionId <String>] [-IncludePathRecommendation <Boolean>] [-Summary <Boolean>] 
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9818f-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="9818f-106">DESCRIPTION</span></span>
<span data-ttu-id="9818f-107">Uyarlamalı uygulama denetimleri otomatik olarak Azure Güvenlik Merkezi tarafından hesaplanıyorsa, aboneliğin kapsamındaki Uyarlamalı uygulama denetimleri kaynaklarının listesini almak için bu cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="9818f-107">Adaptive Application Controls are automatically calculated by Azure Security Center, use this cmdlet to get a list of Adaptive Application Controls resources in the scope of a subscription.</span></span>

## <span data-ttu-id="9818f-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9818f-108">EXAMPLES</span></span>

### <span data-ttu-id="9818f-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9818f-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveApplicationControl
Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP2
Name       : GROUP2
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties

Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP3
Name       : GROUP3
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties

Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP4
Name       : GROUP5
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties

```
<span data-ttu-id="9818f-110">Abonelik için uygulama denetimi VM/sunucu gruplarının bir listesini alır.</span><span class="sxs-lookup"><span data-stu-id="9818f-110">Gets a list of application control VM/server groups for the subscription.</span></span>

## <span data-ttu-id="9818f-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9818f-111">PARAMETERS</span></span>

### <span data-ttu-id="9818f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9818f-112">-DefaultProfile</span></span>
<span data-ttu-id="9818f-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9818f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9818f-114">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="9818f-114">-SubscriptionId</span></span>
<span data-ttu-id="9818f-115">Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="9818f-115">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9818f-116">-Includepathönerilerine</span><span class="sxs-lookup"><span data-stu-id="9818f-116">-IncludePathRecommendations</span></span>
<span data-ttu-id="9818f-117">İlke kurallarını ekleyin.</span><span class="sxs-lookup"><span data-stu-id="9818f-117">Include the policy rules.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: IncludePathRecommendations
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9818f-118">-Özet</span><span class="sxs-lookup"><span data-stu-id="9818f-118">-Summary</span></span>
<span data-ttu-id="9818f-119">Özet formda çıkışı geri döndürme.</span><span class="sxs-lookup"><span data-stu-id="9818f-119">Return output in a summarized form.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: Summary
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9818f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9818f-120">CommonParameters</span></span>
<span data-ttu-id="9818f-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9818f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9818f-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9818f-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9818f-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9818f-123">INPUTS</span></span>

### <span data-ttu-id="9818f-124">System. String</span><span class="sxs-lookup"><span data-stu-id="9818f-124">System.String</span></span>

### <span data-ttu-id="9818f-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9818f-125">System.Boolean</span></span>

## <span data-ttu-id="9818f-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9818f-126">OUTPUTS</span></span>

### <span data-ttu-id="9818f-127">Microsoft. Azure. Commands. Security. model. uyarlanabilir Tiveapplicationcontrols. PSSecurityAdaptiveApplicationControls</span><span class="sxs-lookup"><span data-stu-id="9818f-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span></span>

## <span data-ttu-id="9818f-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9818f-128">NOTES</span></span>

## <span data-ttu-id="9818f-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9818f-129">RELATED LINKS</span></span>
