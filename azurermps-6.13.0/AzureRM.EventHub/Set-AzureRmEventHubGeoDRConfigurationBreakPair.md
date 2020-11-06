---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubGeoDRConfigurationBreakPair.md
ms.openlocfilehash: 3ee0e251f4dd92b087343edc03e829e8032ee5c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590294"
---
# <span data-ttu-id="663c2-101">Set-AzureRmEventHubGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="663c2-101">Set-AzureRmEventHubGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="663c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="663c2-102">SYNOPSIS</span></span>
<span data-ttu-id="663c2-103">Bu işlem olağanüstü durum kurtarması 'nı devre dışı bırakır ve birincil olan değişikliklerin ikincil ad alanlarına çoğaltılmasını durdurur</span><span class="sxs-lookup"><span data-stu-id="663c2-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="663c2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="663c2-104">SYNTAX</span></span>

### <span data-ttu-id="663c2-105">GeoDRParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="663c2-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="663c2-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="663c2-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationBreakPair [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="663c2-107">Geodrconfigresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="663c2-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="663c2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="663c2-108">DESCRIPTION</span></span>
<span data-ttu-id="663c2-109">**Set-AzureRmEventHubGeoDRConfigurationBreakPair** cmdlet</span><span class="sxs-lookup"><span data-stu-id="663c2-109">The **Set-AzureRmEventHubGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="663c2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="663c2-110">EXAMPLES</span></span>

### <span data-ttu-id="663c2-111">Örnekteki</span><span class="sxs-lookup"><span data-stu-id="663c2-111">Example</span></span>
```
PS C:\> Set-AzureRmEventHubGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"
```

<span data-ttu-id="663c2-112">Bu işlem olağanüstü durum kurtarması 'nı devre dışı bırakır ve birincil olan değişikliklerin ikincil ad alanlarına çoğaltılmasını durdurur</span><span class="sxs-lookup"><span data-stu-id="663c2-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="663c2-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="663c2-113">PARAMETERS</span></span>

### <span data-ttu-id="663c2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="663c2-114">-DefaultProfile</span></span>
<span data-ttu-id="663c2-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="663c2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="663c2-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="663c2-116">-InputObject</span></span>
<span data-ttu-id="663c2-117">Eventhub GeoDR yapılandırma nesnesi</span><span class="sxs-lookup"><span data-stu-id="663c2-117">Eventhub GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="663c2-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="663c2-118">-Name</span></span>
<span data-ttu-id="663c2-119">DR yapılandırma adı</span><span class="sxs-lookup"><span data-stu-id="663c2-119">DR Configuration Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="663c2-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="663c2-120">-Namespace</span></span>
<span data-ttu-id="663c2-121">Ad alanı adı-birincil ad alanı</span><span class="sxs-lookup"><span data-stu-id="663c2-121">Namespace Name - Primary Namespace</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="663c2-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="663c2-122">-PassThru</span></span>
<span data-ttu-id="663c2-123">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="663c2-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="663c2-124">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="663c2-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="663c2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="663c2-125">-ResourceGroupName</span></span>
<span data-ttu-id="663c2-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="663c2-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="663c2-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="663c2-127">-ResourceId</span></span>
<span data-ttu-id="663c2-128">GeoDRConfiguration kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="663c2-128">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="663c2-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="663c2-129">-Confirm</span></span>
<span data-ttu-id="663c2-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="663c2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="663c2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="663c2-131">-WhatIf</span></span>
<span data-ttu-id="663c2-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="663c2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="663c2-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="663c2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="663c2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="663c2-134">CommonParameters</span></span>
<span data-ttu-id="663c2-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="663c2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="663c2-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="663c2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="663c2-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="663c2-137">INPUTS</span></span>

### <span data-ttu-id="663c2-138">System. String</span><span class="sxs-lookup"><span data-stu-id="663c2-138">System.String</span></span>

### <span data-ttu-id="663c2-139">Microsoft. Azure. Commands. EventHub. model. Pyetthubdrconfigurationattributes</span><span class="sxs-lookup"><span data-stu-id="663c2-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>
<span data-ttu-id="663c2-140">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="663c2-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="663c2-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="663c2-141">OUTPUTS</span></span>

### <span data-ttu-id="663c2-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="663c2-142">System.Boolean</span></span>

## <span data-ttu-id="663c2-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="663c2-143">NOTES</span></span>

## <span data-ttu-id="663c2-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="663c2-144">RELATED LINKS</span></span>
