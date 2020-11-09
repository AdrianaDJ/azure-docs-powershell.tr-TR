---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 683d03537f410b38260b502bc25ed90c9da9b4d2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319966"
---
# <span data-ttu-id="0c884-101">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="0c884-101">Remove-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="0c884-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c884-102">SYNOPSIS</span></span>
<span data-ttu-id="0c884-103">IoT merkezinizi bir iletinin zenginleştirme.</span><span class="sxs-lookup"><span data-stu-id="0c884-103">Delete a message enrichment in your IoT hub.</span></span>

## <span data-ttu-id="0c884-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0c884-104">SYNTAX</span></span>

### <span data-ttu-id="0c884-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0c884-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c884-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="0c884-106">InputObjectSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c884-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="0c884-107">ResourceIdSet</span></span>
```
Remove-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c884-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0c884-108">DESCRIPTION</span></span>
<span data-ttu-id="0c884-109">Azure IoT Hub 'ındaki ileti zenginleştirme hakkında ayrıntılı bir açıklama için bkz. https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="0c884-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="0c884-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0c884-110">EXAMPLES</span></span>

### <span data-ttu-id="0c884-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0c884-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey" -Passthru

True
```

<span data-ttu-id="0c884-112">"Yenianahtar" ileti zenginleştirme 'yi siler.</span><span class="sxs-lookup"><span data-stu-id="0c884-112">Deletes "newKey" message enrichment.</span></span>

## <span data-ttu-id="0c884-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0c884-113">PARAMETERS</span></span>

### <span data-ttu-id="0c884-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c884-114">-DefaultProfile</span></span>
<span data-ttu-id="0c884-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0c884-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c884-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c884-116">-InputObject</span></span>
<span data-ttu-id="0c884-117">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="0c884-117">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c884-118">-Tuşlu</span><span class="sxs-lookup"><span data-stu-id="0c884-118">-Key</span></span>
<span data-ttu-id="0c884-119">Zenginleştirme tuşu.</span><span class="sxs-lookup"><span data-stu-id="0c884-119">The enrichment's key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c884-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="0c884-120">-Name</span></span>
<span data-ttu-id="0c884-121">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="0c884-121">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c884-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0c884-122">-PassThru</span></span>
<span data-ttu-id="0c884-123">Boole nesnesini döndürmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="0c884-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="0c884-124">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="0c884-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0c884-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c884-125">-ResourceGroupName</span></span>
<span data-ttu-id="0c884-126">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="0c884-126">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c884-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0c884-127">-ResourceId</span></span>
<span data-ttu-id="0c884-128">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="0c884-128">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c884-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="0c884-129">-Confirm</span></span>
<span data-ttu-id="0c884-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0c884-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c884-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c884-131">-WhatIf</span></span>
<span data-ttu-id="0c884-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0c884-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c884-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0c884-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c884-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c884-134">CommonParameters</span></span>
<span data-ttu-id="0c884-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0c884-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c884-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c884-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c884-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0c884-137">INPUTS</span></span>

### <span data-ttu-id="0c884-138">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="0c884-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="0c884-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0c884-139">System.String</span></span>

## <span data-ttu-id="0c884-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0c884-140">OUTPUTS</span></span>

### <span data-ttu-id="0c884-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0c884-141">System.Boolean</span></span>

## <span data-ttu-id="0c884-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0c884-142">NOTES</span></span>

## <span data-ttu-id="0c884-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0c884-143">RELATED LINKS</span></span>
