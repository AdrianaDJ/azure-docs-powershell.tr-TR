---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubedgemodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
ms.openlocfilehash: 5316b6bae6bfc64f791959bb6e236c861833ed4c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280245"
---
# <span data-ttu-id="63527-101">Set-AzIotHubEdgeModule</span><span class="sxs-lookup"><span data-stu-id="63527-101">Set-AzIotHubEdgeModule</span></span>

## <span data-ttu-id="63527-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63527-102">SYNOPSIS</span></span>
<span data-ttu-id="63527-103">Tek bir Edge cihazında Edge modüllerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="63527-103">Set edge modules on a single edge device.</span></span>

## <span data-ttu-id="63527-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="63527-104">SYNTAX</span></span>

### <span data-ttu-id="63527-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="63527-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubEdgeModule [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -ModulesContent <Hashtable> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="63527-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="63527-106">InputObjectSet</span></span>
```
Set-AzIotHubEdgeModule [-InputObject] <PSIotHub> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63527-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="63527-107">ResourceIdSet</span></span>
```
Set-AzIotHubEdgeModule [-ResourceId] <String> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63527-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="63527-108">DESCRIPTION</span></span>
<span data-ttu-id="63527-109">Sağlanan modüller yapılandırma içeriğini belirtilen Edge aygıtına uygular.</span><span class="sxs-lookup"><span data-stu-id="63527-109">Applies the provided modules configuration content to the specified edge device.</span></span>
<span data-ttu-id="63527-110">Not: yürütme sonrasında komut, cihaza uygulanan modül koleksiyonunun çıktısını alır.</span><span class="sxs-lookup"><span data-stu-id="63527-110">Note: Upon execution the command will output the collection of modules applied to the device.</span></span>

## <span data-ttu-id="63527-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="63527-111">EXAMPLES</span></span>

### <span data-ttu-id="63527-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="63527-112">Example 1</span></span>
```powershell
PS C:\> $content = Get-Content "C:/Edge/modules.json" | ConvertFrom-Json -AsHashtable
PS C:\> Set-AzIotHubEdgeModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myEdgeDevice1" -ModulesContent $content
```

<span data-ttu-id="63527-113">Hedef cihazda modüller ayarlayarak geliştirme yaparken Edge modüllerini test etme.</span><span class="sxs-lookup"><span data-stu-id="63527-113">Test edge modules while in development by setting modules on a target device.</span></span>

## <span data-ttu-id="63527-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="63527-114">PARAMETERS</span></span>

### <span data-ttu-id="63527-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63527-115">-DefaultProfile</span></span>
<span data-ttu-id="63527-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="63527-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63527-117">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="63527-117">-DeviceId</span></span>
<span data-ttu-id="63527-118">Hedef Edge cihaz kimliği.</span><span class="sxs-lookup"><span data-stu-id="63527-118">Target Edge Device Id.</span></span>

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

### <span data-ttu-id="63527-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63527-119">-InputObject</span></span>
<span data-ttu-id="63527-120">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="63527-120">IotHub object</span></span>

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

### <span data-ttu-id="63527-121">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="63527-121">-IotHubName</span></span>
<span data-ttu-id="63527-122">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="63527-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="63527-123">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="63527-123">-ModulesContent</span></span>
<span data-ttu-id="63527-124">IoT Edge cihazları için modüllerin yapılandırma içeriği.</span><span class="sxs-lookup"><span data-stu-id="63527-124">Configuration content of modules for IoT Edge devices.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63527-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63527-125">-ResourceGroupName</span></span>
<span data-ttu-id="63527-126">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="63527-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="63527-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="63527-127">-ResourceId</span></span>
<span data-ttu-id="63527-128">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="63527-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="63527-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="63527-129">-Confirm</span></span>
<span data-ttu-id="63527-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="63527-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63527-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63527-131">-WhatIf</span></span>
<span data-ttu-id="63527-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="63527-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63527-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="63527-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63527-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63527-134">CommonParameters</span></span>
<span data-ttu-id="63527-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="63527-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63527-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63527-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63527-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="63527-137">INPUTS</span></span>

### <span data-ttu-id="63527-138">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="63527-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="63527-139">System. String</span><span class="sxs-lookup"><span data-stu-id="63527-139">System.String</span></span>

## <span data-ttu-id="63527-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="63527-140">OUTPUTS</span></span>

### <span data-ttu-id="63527-141">Microsoft. Azure. Commands. Management. IotHub. modeller. PSModules []</span><span class="sxs-lookup"><span data-stu-id="63527-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span></span>

## <span data-ttu-id="63527-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="63527-142">NOTES</span></span>

## <span data-ttu-id="63527-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="63527-143">RELATED LINKS</span></span>
