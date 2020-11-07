---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: b7b1cc38402e69b5783f76ec35445aae7b6944dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751943"
---
# <span data-ttu-id="8e501-101">Remove-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e501-101">Remove-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="8e501-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e501-102">SYNOPSIS</span></span>
<span data-ttu-id="8e501-103">Diğer adı siler (olağanüstü durum kurtarma yapılandırması)</span><span class="sxs-lookup"><span data-stu-id="8e501-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="8e501-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8e501-104">SYNTAX</span></span>

### <span data-ttu-id="8e501-105">GeoDRParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8e501-105">GeoDRParameterSet (Default)</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e501-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8e501-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e501-107">Geodrconfigresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="8e501-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e501-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8e501-108">DESCRIPTION</span></span>
<span data-ttu-id="8e501-109">**Remove-AzEventHubGeoDRConfiguration** cmdlet 'ı bir diğer adı siler (olağanüstü durum kurtarma yapılandırması)</span><span class="sxs-lookup"><span data-stu-id="8e501-109">The **Remove-AzEventHubGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="8e501-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8e501-110">EXAMPLES</span></span>

### <span data-ttu-id="8e501-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8e501-111">Example 1</span></span>
```
PS C:\>Remove-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="8e501-112">Diğer adı siler (olağanüstü durum kurtarma yapılandırması)</span><span class="sxs-lookup"><span data-stu-id="8e501-112">Deletes an Alias (Disaster Recovery configuration)</span></span>

## <span data-ttu-id="8e501-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8e501-113">PARAMETERS</span></span>

### <span data-ttu-id="8e501-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="8e501-114">-AsJob</span></span>
<span data-ttu-id="8e501-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="8e501-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8e501-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e501-116">-DefaultProfile</span></span>
<span data-ttu-id="8e501-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8e501-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e501-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e501-118">-InputObject</span></span>
<span data-ttu-id="8e501-119">Eventhub GeoDR yapılandırma nesnesi</span><span class="sxs-lookup"><span data-stu-id="8e501-119">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="8e501-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="8e501-120">-Name</span></span>
<span data-ttu-id="8e501-121">Diğer ad (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="8e501-121">Alias (GeoDR)</span></span>

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

### <span data-ttu-id="8e501-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8e501-122">-Namespace</span></span>
<span data-ttu-id="8e501-123">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="8e501-123">Namespace Name</span></span>

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

### <span data-ttu-id="8e501-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="8e501-124">-PassThru</span></span>
<span data-ttu-id="8e501-125">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="8e501-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8e501-126">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="8e501-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8e501-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e501-127">-ResourceGroupName</span></span>
<span data-ttu-id="8e501-128">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="8e501-128">Resource Group Name</span></span>

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

### <span data-ttu-id="8e501-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8e501-129">-ResourceId</span></span>
<span data-ttu-id="8e501-130">GeoDRConfiguration kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="8e501-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="8e501-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="8e501-131">-Confirm</span></span>
<span data-ttu-id="8e501-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8e501-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e501-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e501-133">-WhatIf</span></span>
<span data-ttu-id="8e501-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8e501-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e501-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8e501-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e501-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e501-136">CommonParameters</span></span>
<span data-ttu-id="8e501-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8e501-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e501-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e501-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e501-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8e501-139">INPUTS</span></span>

### <span data-ttu-id="8e501-140">System. String</span><span class="sxs-lookup"><span data-stu-id="8e501-140">System.String</span></span>

### <span data-ttu-id="8e501-141">Microsoft. Azure. Commands. EventHub. model. Pyetthubdrconfigurationattributes</span><span class="sxs-lookup"><span data-stu-id="8e501-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="8e501-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8e501-142">OUTPUTS</span></span>

### <span data-ttu-id="8e501-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8e501-143">System.Boolean</span></span>

## <span data-ttu-id="8e501-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8e501-144">NOTES</span></span>

## <span data-ttu-id="8e501-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8e501-145">RELATED LINKS</span></span>
