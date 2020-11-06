---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubGeoDRConfiguration.md
ms.openlocfilehash: 929ebdfb9cc38d5233027da75752f4c82c484536
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590493"
---
# <span data-ttu-id="66ae0-101">Remove-AzureRmEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="66ae0-101">Remove-AzureRmEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="66ae0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66ae0-102">SYNOPSIS</span></span>
<span data-ttu-id="66ae0-103">Diğer adı siler (olağanüstü durum kurtarma yapılandırması)</span><span class="sxs-lookup"><span data-stu-id="66ae0-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66ae0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="66ae0-104">SYNTAX</span></span>

### <span data-ttu-id="66ae0-105">GeoDRParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="66ae0-105">GeoDRParameterSet (Default)</span></span>
```
Remove-AzureRmEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66ae0-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="66ae0-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzureRmEventHubGeoDRConfiguration [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66ae0-107">Geodrconfigresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="66ae0-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzureRmEventHubGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66ae0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="66ae0-108">DESCRIPTION</span></span>
<span data-ttu-id="66ae0-109">**Remove-AzureRmEventHubGeoDRConfiguration** cmdlet 'ı bir diğer adı siler (olağanüstü durum kurtarma yapılandırması)</span><span class="sxs-lookup"><span data-stu-id="66ae0-109">The **Remove-AzureRmEventHubGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="66ae0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="66ae0-110">EXAMPLES</span></span>

### <span data-ttu-id="66ae0-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="66ae0-111">Example 1</span></span>
```
PS C:\>Remove-AzureRmEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="66ae0-112">Diğer adı siler (olağanüstü durum kurtarma yapılandırması)</span><span class="sxs-lookup"><span data-stu-id="66ae0-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="66ae0-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="66ae0-113">PARAMETERS</span></span>

### <span data-ttu-id="66ae0-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="66ae0-114">-AsJob</span></span>
<span data-ttu-id="66ae0-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="66ae0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="66ae0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66ae0-116">-DefaultProfile</span></span>
<span data-ttu-id="66ae0-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="66ae0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66ae0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66ae0-118">-InputObject</span></span>
<span data-ttu-id="66ae0-119">Eventhub GeoDR yapılandırma nesnesi</span><span class="sxs-lookup"><span data-stu-id="66ae0-119">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="66ae0-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="66ae0-120">-Name</span></span>
<span data-ttu-id="66ae0-121">Diğer ad (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="66ae0-121">Alias (GeoDR)</span></span>

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

### <span data-ttu-id="66ae0-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="66ae0-122">-Namespace</span></span>
<span data-ttu-id="66ae0-123">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="66ae0-123">Namespace Name</span></span>

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

### <span data-ttu-id="66ae0-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="66ae0-124">-PassThru</span></span>
<span data-ttu-id="66ae0-125">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="66ae0-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="66ae0-126">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="66ae0-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="66ae0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66ae0-127">-ResourceGroupName</span></span>
<span data-ttu-id="66ae0-128">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="66ae0-128">Resource Group Name</span></span>

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

### <span data-ttu-id="66ae0-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="66ae0-129">-ResourceId</span></span>
<span data-ttu-id="66ae0-130">GeoDRConfiguration kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="66ae0-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="66ae0-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="66ae0-131">-Confirm</span></span>
<span data-ttu-id="66ae0-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="66ae0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66ae0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66ae0-133">-WhatIf</span></span>
<span data-ttu-id="66ae0-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="66ae0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66ae0-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="66ae0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66ae0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66ae0-136">CommonParameters</span></span>
<span data-ttu-id="66ae0-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="66ae0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="66ae0-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66ae0-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66ae0-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="66ae0-139">INPUTS</span></span>

### <span data-ttu-id="66ae0-140">System. String</span><span class="sxs-lookup"><span data-stu-id="66ae0-140">System.String</span></span>
<span data-ttu-id="66ae0-141">Microsoft. Azure. Commands. EventHub. model. Pyetthubdrconfigurationattributes</span><span class="sxs-lookup"><span data-stu-id="66ae0-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>


## <span data-ttu-id="66ae0-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="66ae0-142">OUTPUTS</span></span>

### <span data-ttu-id="66ae0-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="66ae0-143">System.Boolean</span></span>


## <span data-ttu-id="66ae0-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="66ae0-144">NOTES</span></span>

## <span data-ttu-id="66ae0-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="66ae0-145">RELATED LINKS</span></span>
