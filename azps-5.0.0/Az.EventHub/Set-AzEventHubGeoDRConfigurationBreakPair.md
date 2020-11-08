---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
ms.openlocfilehash: f343b92452a34a746d9ff09d5a519519aeaa7a6c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277437"
---
# <span data-ttu-id="c5759-101">Set-AzEventHubGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="c5759-101">Set-AzEventHubGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="c5759-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5759-102">SYNOPSIS</span></span>
<span data-ttu-id="c5759-103">Bu işlem olağanüstü durum kurtarması 'nı devre dışı bırakır ve birincil olan değişikliklerin ikincil ad alanlarına çoğaltılmasını durdurur</span><span class="sxs-lookup"><span data-stu-id="c5759-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="c5759-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c5759-104">SYNTAX</span></span>

### <span data-ttu-id="c5759-105">GeoDRParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c5759-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5759-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c5759-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5759-107">Geodrconfigresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="c5759-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5759-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c5759-108">DESCRIPTION</span></span>
<span data-ttu-id="c5759-109">**Set-AzEventHubGeoDRConfigurationBreakPair** cmdlet 'ı etkisiz kurtarma</span><span class="sxs-lookup"><span data-stu-id="c5759-109">The **Set-AzEventHubGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="c5759-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c5759-110">EXAMPLES</span></span>

### <span data-ttu-id="c5759-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c5759-111">Example 1</span></span>
```powershell
PS C:\> Set-AzEventHubGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"
```

<span data-ttu-id="c5759-112">Bu işlem olağanüstü durum kurtarması 'nı devre dışı bırakır ve birincil olan değişikliklerin ikincil ad alanlarına çoğaltılmasını durdurur</span><span class="sxs-lookup"><span data-stu-id="c5759-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="c5759-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c5759-113">PARAMETERS</span></span>

### <span data-ttu-id="c5759-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5759-114">-DefaultProfile</span></span>
<span data-ttu-id="c5759-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c5759-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5759-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5759-116">-InputObject</span></span>
<span data-ttu-id="c5759-117">Eventhub GeoDR yapılandırma nesnesi</span><span class="sxs-lookup"><span data-stu-id="c5759-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="c5759-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="c5759-118">-Name</span></span>
<span data-ttu-id="c5759-119">DR yapılandırma adı</span><span class="sxs-lookup"><span data-stu-id="c5759-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="c5759-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c5759-120">-Namespace</span></span>
<span data-ttu-id="c5759-121">Ad alanı adı-birincil ad alanı</span><span class="sxs-lookup"><span data-stu-id="c5759-121">Namespace Name - Primary Namespace</span></span>

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

### <span data-ttu-id="c5759-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c5759-122">-PassThru</span></span>
<span data-ttu-id="c5759-123">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="c5759-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c5759-124">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="c5759-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c5759-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5759-125">-ResourceGroupName</span></span>
<span data-ttu-id="c5759-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="c5759-126">Resource Group Name</span></span>

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

### <span data-ttu-id="c5759-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c5759-127">-ResourceId</span></span>
<span data-ttu-id="c5759-128">GeoDRConfiguration kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="c5759-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="c5759-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="c5759-129">-Confirm</span></span>
<span data-ttu-id="c5759-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c5759-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5759-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5759-131">-WhatIf</span></span>
<span data-ttu-id="c5759-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c5759-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5759-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c5759-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5759-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5759-134">CommonParameters</span></span>
<span data-ttu-id="c5759-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c5759-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5759-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5759-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5759-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c5759-137">INPUTS</span></span>

### <span data-ttu-id="c5759-138">System. String</span><span class="sxs-lookup"><span data-stu-id="c5759-138">System.String</span></span>

### <span data-ttu-id="c5759-139">Microsoft. Azure. Commands. EventHub. model. Pyetthubdrconfigurationattributes</span><span class="sxs-lookup"><span data-stu-id="c5759-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="c5759-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c5759-140">OUTPUTS</span></span>

### <span data-ttu-id="c5759-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c5759-141">System.Boolean</span></span>

## <span data-ttu-id="c5759-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c5759-142">NOTES</span></span>

## <span data-ttu-id="c5759-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c5759-143">RELATED LINKS</span></span>
