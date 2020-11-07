---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/revoke-azdatasharesubscriptionaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Revoke-AzDataShareSubscriptionAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Revoke-AzDataShareSubscriptionAccess.md
ms.openlocfilehash: 93e0aa57a418af038a397559959b40500ad58af3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752160"
---
# <span data-ttu-id="2c4ee-101">Revoke-AzDataShareSubscriptionAccess</span><span class="sxs-lookup"><span data-stu-id="2c4ee-101">Revoke-AzDataShareSubscriptionAccess</span></span>

## <span data-ttu-id="2c4ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c4ee-102">SYNOPSIS</span></span>
<span data-ttu-id="2c4ee-103">Aboneliği kaldırma</span><span class="sxs-lookup"><span data-stu-id="2c4ee-103">Revokes share subscription access to source share</span></span>

## <span data-ttu-id="2c4ee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2c4ee-104">SYNTAX</span></span>

### <span data-ttu-id="2c4ee-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2c4ee-105">ByFieldsParameterSet (Default)</span></span>
```
Revoke-AzDataShareSubscriptionAccess -ResourceGroupName <String> -AccountName <String> [-ShareName <String>]
 -ShareSubscriptionId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2c4ee-106">Byprovidersharesubscriptionıdparameterset</span><span class="sxs-lookup"><span data-stu-id="2c4ee-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Revoke-AzDataShareSubscriptionAccess -ShareSubscriptionId <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c4ee-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2c4ee-107">DESCRIPTION</span></span>
<span data-ttu-id="2c4ee-108">**Revoke-AzDataShareSubscriptionAccess** cmdlet 'i kaynak paylaşımına bir abonelik paylaşımı erişimi verir</span><span class="sxs-lookup"><span data-stu-id="2c4ee-108">The **Revoke-AzDataShareSubscriptionAccess** cmdlet grants a share subscription access to source share</span></span>

## <span data-ttu-id="2c4ee-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2c4ee-109">EXAMPLES</span></span>

### <span data-ttu-id="2c4ee-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2c4ee-110">Example 1</span></span>
```
PS C:\> Revoke-AzDataShareSubscriptionAccess -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -ShareName "AdsShare" -ShareSubscriptionId 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12

Company                   : ADS
CreatedAt                 : 6/15/2019 1:02:28 AM
CreatedBy                 : abc@microsoft.com
SharedAt                  : 6/15/2019 12:08:48 AM
SharedBy                  : abc@microsoft.com
ShareSubscriptionObjectId : 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12
ShareSubscriptionStatus   : Revoked
Id                        : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare/shareSubscriptions/8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12
Name                      : AdsShare
Type                      : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="2c4ee-111">Kimlik 8EE,6e6fd-b4a1-49a4-bb66-f187f38e0e12 ile tanımlanan paylaşım aboneliğine erişimi iptal eder</span><span class="sxs-lookup"><span data-stu-id="2c4ee-111">Revokes access of share subscription identified by id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span></span>

## <span data-ttu-id="2c4ee-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2c4ee-112">PARAMETERS</span></span>

### <span data-ttu-id="2c4ee-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2c4ee-113">-AccountName</span></span>
<span data-ttu-id="2c4ee-114">Azure veri paylaşımı hesap adı</span><span class="sxs-lookup"><span data-stu-id="2c4ee-114">Azure data share account name</span></span>

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

### <span data-ttu-id="2c4ee-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="2c4ee-115">-AsJob</span></span>
<span data-ttu-id="2c4ee-116">{{Fill Iş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="2c4ee-116">{{Fill AsJob Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c4ee-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c4ee-117">-DefaultProfile</span></span>
<span data-ttu-id="2c4ee-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2c4ee-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c4ee-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c4ee-119">-ResourceGroupName</span></span>
<span data-ttu-id="2c4ee-120">Azure veri paylaşımı hesabının kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="2c4ee-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="2c4ee-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2c4ee-121">-ResourceId</span></span>
<span data-ttu-id="2c4ee-122">Azure veri paylaşımı 'nın kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="2c4ee-122">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="2c4ee-123">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="2c4ee-123">-ShareName</span></span>
<span data-ttu-id="2c4ee-124">Azure veri paylaşımı adı</span><span class="sxs-lookup"><span data-stu-id="2c4ee-124">Azure data share name</span></span>

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

### <span data-ttu-id="2c4ee-125">-Sharesubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="2c4ee-125">-ShareSubscriptionId</span></span>
<span data-ttu-id="2c4ee-126">Sağlayıcı paylaşım aboneliğinin paylaşım aboneliği kimliği</span><span class="sxs-lookup"><span data-stu-id="2c4ee-126">The share subscription id of the provider share subscription</span></span>

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

### <span data-ttu-id="2c4ee-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="2c4ee-127">-Confirm</span></span>
<span data-ttu-id="2c4ee-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2c4ee-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c4ee-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c4ee-129">-WhatIf</span></span>
<span data-ttu-id="2c4ee-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2c4ee-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c4ee-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2c4ee-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c4ee-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c4ee-132">CommonParameters</span></span>
<span data-ttu-id="2c4ee-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2c4ee-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c4ee-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c4ee-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c4ee-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2c4ee-135">INPUTS</span></span>

### <span data-ttu-id="2c4ee-136">System. String</span><span class="sxs-lookup"><span data-stu-id="2c4ee-136">System.String</span></span>

## <span data-ttu-id="2c4ee-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2c4ee-137">OUTPUTS</span></span>

### <span data-ttu-id="2c4ee-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="2c4ee-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="2c4ee-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2c4ee-139">NOTES</span></span>

## <span data-ttu-id="2c4ee-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2c4ee-140">RELATED LINKS</span></span>