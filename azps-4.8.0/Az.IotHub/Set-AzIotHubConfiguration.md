---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
ms.openlocfilehash: 9b6c9b77ae29214c7d998e3d2c859e4ac7521db1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267224"
---
# <span data-ttu-id="70c17-101">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="70c17-101">Set-AzIotHubConfiguration</span></span>

## <span data-ttu-id="70c17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70c17-102">SYNOPSIS</span></span>
<span data-ttu-id="70c17-103">Yapılandırma kaydının kesilebilir alanlarını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="70c17-103">Update the mutable fields of the configuration registration.</span></span>

## <span data-ttu-id="70c17-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="70c17-104">SYNTAX</span></span>

### <span data-ttu-id="70c17-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="70c17-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name] <String>
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70c17-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="70c17-106">InputObjectSet</span></span>
```
Set-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70c17-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="70c17-107">ResourceIdSet</span></span>
```
Set-AzIotHubConfiguration [-ResourceId] <String> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70c17-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="70c17-108">DESCRIPTION</span></span>
<span data-ttu-id="70c17-109">IoT otomatik cihaz yönetimi yapılandırmasının belirtilen özelliklerini güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="70c17-109">Update specified properties of an IoT automatic device management configuration.</span></span>
<span data-ttu-id="70c17-110">Not: yapılandırma içeriği sabittir.</span><span class="sxs-lookup"><span data-stu-id="70c17-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="70c17-111">Güncelleştirilebilen yapılandırma özellikleri ' Etiketler ', ' ölçümler ', ' öncelik ' ve ' Targetkoşul '.</span><span class="sxs-lookup"><span data-stu-id="70c17-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="70c17-112"> https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-managementDaha fazla bilgi için bkz.</span><span class="sxs-lookup"><span data-stu-id="70c17-112">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="70c17-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="70c17-113">EXAMPLES</span></span>

### <span data-ttu-id="70c17-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="70c17-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="70c17-115">Cihaz yapılandırmasının önceliğini değiştirme ve hedef koşulunu güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="70c17-115">Alter the priority of a device configuration and update its target condition</span></span>

## <span data-ttu-id="70c17-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="70c17-116">PARAMETERS</span></span>

### <span data-ttu-id="70c17-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70c17-117">-DefaultProfile</span></span>
<span data-ttu-id="70c17-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="70c17-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70c17-119">-Force</span><span class="sxs-lookup"><span data-stu-id="70c17-119">-Force</span></span>
<span data-ttu-id="70c17-120">Son kez alınmasından itibaren güncelleştirilse bile yapılandırma nesnesinin değiştirilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="70c17-120">Allows configuration object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="70c17-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70c17-121">-InputObject</span></span>
<span data-ttu-id="70c17-122">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="70c17-122">IotHub object</span></span>

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

### <span data-ttu-id="70c17-123">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="70c17-123">-IotHubName</span></span>
<span data-ttu-id="70c17-124">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="70c17-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="70c17-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="70c17-125">-Label</span></span>
<span data-ttu-id="70c17-126">Hedef yapılandırmaya uygulanacak etiketlerin haritası.</span><span class="sxs-lookup"><span data-stu-id="70c17-126">Map of labels to be applied to target configuration.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70c17-127">-Metrik</span><span class="sxs-lookup"><span data-stu-id="70c17-127">-Metric</span></span>
<span data-ttu-id="70c17-128">Yapılandırma ölçümleri tanımı için sorgular koleksiyonu.</span><span class="sxs-lookup"><span data-stu-id="70c17-128">Queries collection for configuration metrics definition.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70c17-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="70c17-129">-Name</span></span>
<span data-ttu-id="70c17-130">Yapılandırma kimliği.</span><span class="sxs-lookup"><span data-stu-id="70c17-130">Identifier for the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70c17-131">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="70c17-131">-Priority</span></span>
<span data-ttu-id="70c17-132">Rekabet kuralları (en yüksek WINS) durumunda cihaz yapılandırmasının ağırlığı.</span><span class="sxs-lookup"><span data-stu-id="70c17-132">Weight of the device configuration in case of competing rules (highest wins).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70c17-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70c17-133">-ResourceGroupName</span></span>
<span data-ttu-id="70c17-134">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="70c17-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="70c17-135">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="70c17-135">-ResourceId</span></span>
<span data-ttu-id="70c17-136">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="70c17-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="70c17-137">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="70c17-137">-TargetCondition</span></span>
<span data-ttu-id="70c17-138">Cihaz yapılandırmasının uygulandığı hedef koşulu.</span><span class="sxs-lookup"><span data-stu-id="70c17-138">Target condition in which a device configuration applies to.</span></span>

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

### <span data-ttu-id="70c17-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="70c17-139">-Confirm</span></span>
<span data-ttu-id="70c17-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="70c17-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70c17-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70c17-141">-WhatIf</span></span>
<span data-ttu-id="70c17-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="70c17-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70c17-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="70c17-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70c17-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70c17-144">CommonParameters</span></span>
<span data-ttu-id="70c17-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="70c17-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70c17-146">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70c17-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70c17-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="70c17-147">INPUTS</span></span>

### <span data-ttu-id="70c17-148">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="70c17-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="70c17-149">System. String</span><span class="sxs-lookup"><span data-stu-id="70c17-149">System.String</span></span>

## <span data-ttu-id="70c17-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="70c17-150">OUTPUTS</span></span>

### <span data-ttu-id="70c17-151">Microsoft. Azure. Commands. Management. IotHub. modeller. PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="70c17-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="70c17-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="70c17-152">NOTES</span></span>

## <span data-ttu-id="70c17-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="70c17-153">RELATED LINKS</span></span>
