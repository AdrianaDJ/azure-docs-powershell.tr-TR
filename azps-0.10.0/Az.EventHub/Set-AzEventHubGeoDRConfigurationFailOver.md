---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
ms.openlocfilehash: 6569c5081ec92e20682edf63c09f1b4319d4c038
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935851"
---
# <span data-ttu-id="a0f42-101">Set-AzEventHubGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="a0f42-101">Set-AzEventHubGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="a0f42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0f42-102">SYNOPSIS</span></span>
<span data-ttu-id="a0f42-103">COĞRAFI DR yük devretmesini başlatır ve diğer adı ikincil ad alanına işaret edecek şekilde yeniden yapılandırın</span><span class="sxs-lookup"><span data-stu-id="a0f42-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="a0f42-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a0f42-104">SYNTAX</span></span>

### <span data-ttu-id="a0f42-105">GeoDRParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a0f42-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0f42-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a0f42-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0f42-107">Geodrconfigresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="a0f42-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0f42-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a0f42-108">DESCRIPTION</span></span>
<span data-ttu-id="a0f42-109">**Set-AzEventHubGeoDRConfigurationFailOver** cmdlet 'ı, coğrafi</span><span class="sxs-lookup"><span data-stu-id="a0f42-109">The **Set-AzEventHubGeoDRConfigurationFailOver** cmdlet invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="a0f42-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a0f42-110">EXAMPLES</span></span>

### <span data-ttu-id="a0f42-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a0f42-111">Example 1</span></span>
```
PS C:\>Set-AzEventHubGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="a0f42-112">"SampleDRConfigName" diğer adı üzerinden yük devretmeyi çağırır, yeniden yapılandırır ve "SampleNamespace_Secondary" Ikincil ad alanını işaret eder</span><span class="sxs-lookup"><span data-stu-id="a0f42-112">Invokes the Failover over alias "SampleDRConfigName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="a0f42-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a0f42-113">PARAMETERS</span></span>

### <span data-ttu-id="a0f42-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0f42-114">-DefaultProfile</span></span>
<span data-ttu-id="a0f42-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a0f42-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0f42-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0f42-116">-InputObject</span></span>
<span data-ttu-id="a0f42-117">Eventhub GeoDR yapılandırma nesnesi</span><span class="sxs-lookup"><span data-stu-id="a0f42-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="a0f42-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="a0f42-118">-Name</span></span>
<span data-ttu-id="a0f42-119">DR yapılandırma adı</span><span class="sxs-lookup"><span data-stu-id="a0f42-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="a0f42-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a0f42-120">-Namespace</span></span>
<span data-ttu-id="a0f42-121">Ad alanı adı-Ikincil ad alanı</span><span class="sxs-lookup"><span data-stu-id="a0f42-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="a0f42-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a0f42-122">-PassThru</span></span>
<span data-ttu-id="a0f42-123">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="a0f42-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a0f42-124">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="a0f42-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a0f42-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0f42-125">-ResourceGroupName</span></span>
<span data-ttu-id="a0f42-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="a0f42-126">Resource Group Name</span></span>

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

### <span data-ttu-id="a0f42-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a0f42-127">-ResourceId</span></span>
<span data-ttu-id="a0f42-128">GeoDRConfiguration kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="a0f42-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="a0f42-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="a0f42-129">-Confirm</span></span>
<span data-ttu-id="a0f42-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a0f42-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0f42-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0f42-131">-WhatIf</span></span>
<span data-ttu-id="a0f42-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a0f42-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0f42-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a0f42-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0f42-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0f42-134">CommonParameters</span></span>
<span data-ttu-id="a0f42-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a0f42-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0f42-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0f42-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0f42-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a0f42-137">INPUTS</span></span>

### <span data-ttu-id="a0f42-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a0f42-138">System.String</span></span>

### <span data-ttu-id="a0f42-139">Microsoft. Azure. Commands. EventHub. model. Pyetthubdrconfigurationattributes</span><span class="sxs-lookup"><span data-stu-id="a0f42-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="a0f42-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a0f42-140">OUTPUTS</span></span>

### <span data-ttu-id="a0f42-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a0f42-141">System.Boolean</span></span>

## <span data-ttu-id="a0f42-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a0f42-142">NOTES</span></span>

## <span data-ttu-id="a0f42-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a0f42-143">RELATED LINKS</span></span>
