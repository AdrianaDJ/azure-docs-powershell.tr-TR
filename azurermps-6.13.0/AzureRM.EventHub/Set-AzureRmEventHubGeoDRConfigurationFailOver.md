---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubGeoDRConfigurationFailOver.md
ms.openlocfilehash: 84a101a427fc5541d4888a0b4deb4c5e3880b1d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590292"
---
# <span data-ttu-id="a5e45-101">Set-AzureRmEventHubGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="a5e45-101">Set-AzureRmEventHubGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="a5e45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5e45-102">SYNOPSIS</span></span>
<span data-ttu-id="a5e45-103">COĞRAFI DR yük devretmesini başlatır ve diğer adı ikincil ad alanına işaret edecek şekilde yeniden yapılandırın</span><span class="sxs-lookup"><span data-stu-id="a5e45-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5e45-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a5e45-104">SYNTAX</span></span>

### <span data-ttu-id="a5e45-105">GeoDRParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a5e45-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5e45-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a5e45-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationFailOver [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5e45-107">Geodrconfigresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="a5e45-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5e45-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a5e45-108">DESCRIPTION</span></span>
<span data-ttu-id="a5e45-109">**Set-AzureRmEventHubGeoDRConfigurationFailOver** cmdlet 'ı, coğrafi Dr yerine çalışma</span><span class="sxs-lookup"><span data-stu-id="a5e45-109">The **Set-AzureRmEventHubGeoDRConfigurationFailOver** cmdlet envokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="a5e45-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a5e45-110">EXAMPLES</span></span>

### <span data-ttu-id="a5e45-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a5e45-111">Example 1</span></span>
```
PS C:\>Set-AzureRmEventHubGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="a5e45-112">"SampleDRCongifName" diğer adı üzerinden yük devretmeyi çağırır, yeniden yapılandırır ve "SampleNamespace_Secondary" Ikincil ad alanını işaret edin</span><span class="sxs-lookup"><span data-stu-id="a5e45-112">Invokes the Failover over alias "SampleDRCongifName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="a5e45-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a5e45-113">PARAMETERS</span></span>

### <span data-ttu-id="a5e45-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5e45-114">-DefaultProfile</span></span>
<span data-ttu-id="a5e45-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a5e45-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5e45-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5e45-116">-InputObject</span></span>
<span data-ttu-id="a5e45-117">Eventhub GeoDR yapılandırma nesnesi</span><span class="sxs-lookup"><span data-stu-id="a5e45-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="a5e45-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="a5e45-118">-Name</span></span>
<span data-ttu-id="a5e45-119">DR yapılandırma adı</span><span class="sxs-lookup"><span data-stu-id="a5e45-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="a5e45-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a5e45-120">-Namespace</span></span>
<span data-ttu-id="a5e45-121">Ad alanı adı-Ikincil ad alanı</span><span class="sxs-lookup"><span data-stu-id="a5e45-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="a5e45-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a5e45-122">-PassThru</span></span>
<span data-ttu-id="a5e45-123">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="a5e45-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a5e45-124">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="a5e45-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a5e45-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5e45-125">-ResourceGroupName</span></span>
<span data-ttu-id="a5e45-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="a5e45-126">Resource Group Name</span></span>

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

### <span data-ttu-id="a5e45-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a5e45-127">-ResourceId</span></span>
<span data-ttu-id="a5e45-128">GeoDRConfiguration kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="a5e45-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="a5e45-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="a5e45-129">-Confirm</span></span>
<span data-ttu-id="a5e45-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a5e45-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5e45-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5e45-131">-WhatIf</span></span>
<span data-ttu-id="a5e45-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a5e45-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5e45-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a5e45-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5e45-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5e45-134">CommonParameters</span></span>
<span data-ttu-id="a5e45-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a5e45-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5e45-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5e45-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5e45-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a5e45-137">INPUTS</span></span>

### <span data-ttu-id="a5e45-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a5e45-138">System.String</span></span>

### <span data-ttu-id="a5e45-139">Microsoft. Azure. Commands. EventHub. model. Pyetthubdrconfigurationattributes</span><span class="sxs-lookup"><span data-stu-id="a5e45-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>
<span data-ttu-id="a5e45-140">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a5e45-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="a5e45-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a5e45-141">OUTPUTS</span></span>

### <span data-ttu-id="a5e45-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a5e45-142">System.Boolean</span></span>

## <span data-ttu-id="a5e45-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a5e45-143">NOTES</span></span>

## <span data-ttu-id="a5e45-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a5e45-144">RELATED LINKS</span></span>
