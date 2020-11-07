---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubGeoDRConfigurationBreakPair.md
ms.openlocfilehash: e6dea50e3cb9933d9c6a8aa141f2df43be0b1a18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762734"
---
# <span data-ttu-id="66ec3-101">Set-AzureRmEventHubGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="66ec3-101">Set-AzureRmEventHubGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="66ec3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66ec3-102">SYNOPSIS</span></span>
<span data-ttu-id="66ec3-103">Bu işlem olağanüstü durum kurtarması 'nı devre dışı bırakır ve birincil olan değişikliklerin ikincil ad alanlarına çoğaltılmasını durdurur</span><span class="sxs-lookup"><span data-stu-id="66ec3-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66ec3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="66ec3-104">SYNTAX</span></span>

### <span data-ttu-id="66ec3-105">GeoDRParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="66ec3-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66ec3-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="66ec3-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationBreakPair [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66ec3-107">Geodrconfigresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="66ec3-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66ec3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="66ec3-108">DESCRIPTION</span></span>
<span data-ttu-id="66ec3-109">**Set-AzureRmEventHubGeoDRConfigurationBreakPair** cmdlet</span><span class="sxs-lookup"><span data-stu-id="66ec3-109">The **Set-AzureRmEventHubGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="66ec3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="66ec3-110">EXAMPLES</span></span>

### <span data-ttu-id="66ec3-111">Örnekteki</span><span class="sxs-lookup"><span data-stu-id="66ec3-111">Example</span></span>
```
PS C:\> Set-AzureRmEventHubGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"
```

<span data-ttu-id="66ec3-112">Bu işlem olağanüstü durum kurtarması 'nı devre dışı bırakır ve birincil olan değişikliklerin ikincil ad alanlarına çoğaltılmasını durdurur</span><span class="sxs-lookup"><span data-stu-id="66ec3-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="66ec3-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="66ec3-113">PARAMETERS</span></span>

### <span data-ttu-id="66ec3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66ec3-114">-DefaultProfile</span></span>
<span data-ttu-id="66ec3-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="66ec3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66ec3-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66ec3-116">-InputObject</span></span>
<span data-ttu-id="66ec3-117">Eventhub GeoDR yapılandırma nesnesi</span><span class="sxs-lookup"><span data-stu-id="66ec3-117">Eventhub GeoDR Configuration Object</span></span>

```yaml
Type: PSEventHubDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66ec3-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="66ec3-118">-Name</span></span>
<span data-ttu-id="66ec3-119">DR yapılandırma adı</span><span class="sxs-lookup"><span data-stu-id="66ec3-119">DR Configuration Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66ec3-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="66ec3-120">-Namespace</span></span>
<span data-ttu-id="66ec3-121">Ad alanı adı-birincil ad alanı</span><span class="sxs-lookup"><span data-stu-id="66ec3-121">Namespace Name - Primary Namespace</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66ec3-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="66ec3-122">-PassThru</span></span>
<span data-ttu-id="66ec3-123">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="66ec3-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="66ec3-124">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="66ec3-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66ec3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66ec3-125">-ResourceGroupName</span></span>
<span data-ttu-id="66ec3-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="66ec3-126">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66ec3-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="66ec3-127">-ResourceId</span></span>
<span data-ttu-id="66ec3-128">GeoDRConfiguration kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="66ec3-128">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66ec3-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="66ec3-129">-Confirm</span></span>
<span data-ttu-id="66ec3-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="66ec3-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66ec3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66ec3-131">-WhatIf</span></span>
<span data-ttu-id="66ec3-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="66ec3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66ec3-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="66ec3-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66ec3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66ec3-134">CommonParameters</span></span>
<span data-ttu-id="66ec3-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="66ec3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="66ec3-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66ec3-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66ec3-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="66ec3-137">INPUTS</span></span>

### <span data-ttu-id="66ec3-138">System. String</span><span class="sxs-lookup"><span data-stu-id="66ec3-138">System.String</span></span>
<span data-ttu-id="66ec3-139">Microsoft. Azure. Commands. EventHub. model. Pyetthubdrconfigurationattributes</span><span class="sxs-lookup"><span data-stu-id="66ec3-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>


## <span data-ttu-id="66ec3-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="66ec3-140">OUTPUTS</span></span>

### <span data-ttu-id="66ec3-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="66ec3-141">System.Boolean</span></span>


## <span data-ttu-id="66ec3-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="66ec3-142">NOTES</span></span>

## <span data-ttu-id="66ec3-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="66ec3-143">RELATED LINKS</span></span>
