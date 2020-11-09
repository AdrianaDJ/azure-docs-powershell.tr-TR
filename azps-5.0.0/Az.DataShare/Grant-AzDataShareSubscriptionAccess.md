---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/grant-azdatasharesubscriptionaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Grant-AzDataShareSubscriptionAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Grant-AzDataShareSubscriptionAccess.md
ms.openlocfilehash: 4ad530fdd27c3b87b8e96e1752c00fc149c1dd42
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320321"
---
# <span data-ttu-id="cf60d-101">Grant-AzDataShareSubscriptionAccess</span><span class="sxs-lookup"><span data-stu-id="cf60d-101">Grant-AzDataShareSubscriptionAccess</span></span>

## <span data-ttu-id="cf60d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf60d-102">SYNOPSIS</span></span>
<span data-ttu-id="cf60d-103">İptal edilen bir paylaşım aboneliği kaynak paylaşımına erişimi verir</span><span class="sxs-lookup"><span data-stu-id="cf60d-103">Grants a revoked share subscription access to source share</span></span>

## <span data-ttu-id="cf60d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cf60d-104">SYNTAX</span></span>

### <span data-ttu-id="cf60d-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cf60d-105">ByFieldsParameterSet (Default)</span></span>
```
Grant-AzDataShareSubscriptionAccess -ResourceGroupName <String> -AccountName <String> [-ShareName <String>]
 -ShareSubscriptionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cf60d-106">Byprovidersharesubscriptionıdparameterset</span><span class="sxs-lookup"><span data-stu-id="cf60d-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Grant-AzDataShareSubscriptionAccess -ShareSubscriptionId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf60d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="cf60d-107">DESCRIPTION</span></span>
<span data-ttu-id="cf60d-108">**Grant-AzDataShareSubscriptionAccess** cmdlet 'i kaynak paylaşımına bir abonelik paylaşımı erişimi verir</span><span class="sxs-lookup"><span data-stu-id="cf60d-108">The **Grant-AzDataShareSubscriptionAccess** cmdlet grants a share subscription access to source share</span></span>

## <span data-ttu-id="cf60d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cf60d-109">EXAMPLES</span></span>

### <span data-ttu-id="cf60d-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cf60d-110">Example 1</span></span>
```
PS C:\> Grant-AzDataShareSubscriptionAccess -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -ShareName "AdsShare" -ShareSubscriptionId 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12

Company                   : ADS
CreatedAt                 : 6/15/2019 1:02:28 AM
CreatedBy                 : abc@microsoft.com
SharedAt                  : 6/15/2019 12:08:48 AM
SharedBy                  : abc@microsoft.com
ShareSubscriptionObjectId : 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12
ShareSubscriptionStatus   : Active
Id                        : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare/shareSubscriptions/8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12
Name                      : AdsShare
Type                      : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="cf60d-111">Kimlik 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12 ile tanımlanan paylaşım aboneliğine erişim izni verir</span><span class="sxs-lookup"><span data-stu-id="cf60d-111">Grants access to share subscription identified by id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span></span>

## <span data-ttu-id="cf60d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cf60d-112">PARAMETERS</span></span>

### <span data-ttu-id="cf60d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cf60d-113">-AccountName</span></span>
<span data-ttu-id="cf60d-114">Azure veri paylaşımı hesap adı</span><span class="sxs-lookup"><span data-stu-id="cf60d-114">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf60d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf60d-115">-DefaultProfile</span></span>
<span data-ttu-id="cf60d-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cf60d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf60d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf60d-117">-ResourceGroupName</span></span>
<span data-ttu-id="cf60d-118">Azure veri paylaşımı hesabının kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="cf60d-118">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf60d-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="cf60d-119">-ResourceId</span></span>
<span data-ttu-id="cf60d-120">Azure veri paylaşımı 'nın kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="cf60d-120">The resource id of the azure data share</span></span>

```yaml
Type: System.String
Parameter Sets: ByProviderShareSubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf60d-121">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="cf60d-121">-ShareName</span></span>
<span data-ttu-id="cf60d-122">Azure veri paylaşımı adı</span><span class="sxs-lookup"><span data-stu-id="cf60d-122">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf60d-123">-Sharesubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="cf60d-123">-ShareSubscriptionId</span></span>
<span data-ttu-id="cf60d-124">Sağlayıcı paylaşım aboneliğinin paylaşım aboneliği kimliği</span><span class="sxs-lookup"><span data-stu-id="cf60d-124">The share subscription id of the provider share subscription</span></span>

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

### <span data-ttu-id="cf60d-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="cf60d-125">-Confirm</span></span>
<span data-ttu-id="cf60d-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cf60d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf60d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf60d-127">-WhatIf</span></span>
<span data-ttu-id="cf60d-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cf60d-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cf60d-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cf60d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf60d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf60d-130">CommonParameters</span></span>
<span data-ttu-id="cf60d-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cf60d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf60d-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="cf60d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf60d-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cf60d-133">INPUTS</span></span>

### <span data-ttu-id="cf60d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="cf60d-134">System.String</span></span>

## <span data-ttu-id="cf60d-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cf60d-135">OUTPUTS</span></span>

### <span data-ttu-id="cf60d-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="cf60d-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="cf60d-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cf60d-137">NOTES</span></span>

## <span data-ttu-id="cf60d-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cf60d-138">RELATED LINKS</span></span>
