---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
ms.openlocfilehash: 486ca6543bb32d096e454d16ff3640720f2f53fe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108248"
---
# <span data-ttu-id="9190f-101">New-AzIotHubSasToken</span><span class="sxs-lookup"><span data-stu-id="9190f-101">New-AzIotHubSasToken</span></span>

## <span data-ttu-id="9190f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9190f-102">SYNOPSIS</span></span>
<span data-ttu-id="9190f-103">Hedef IoT Merkezi, cihaz veya modül için SAS belirteci oluşturun.</span><span class="sxs-lookup"><span data-stu-id="9190f-103">Generate a SAS token for a target IoT Hub, device or module.</span></span>

## <span data-ttu-id="9190f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9190f-104">SYNTAX</span></span>

### <span data-ttu-id="9190f-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9190f-105">ResourceSet (Default)</span></span>
```
New-AzIotHubSasToken [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-ModuleId <String>] [-KeyName <String>] [-KeyType <PSKeyType>] [-Duration <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9190f-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="9190f-106">InputObjectSet</span></span>
```
New-AzIotHubSasToken [-InputObject] <PSIotHub> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9190f-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="9190f-107">ResourceIdSet</span></span>
```
New-AzIotHubSasToken [-ResourceId] <String> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9190f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9190f-108">DESCRIPTION</span></span>
<span data-ttu-id="9190f-109">Cihaz SAS belirteçleri için, ilke parametresi yalnızca cihaz kayıt defterine erişmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9190f-109">For device SAS tokens, the policy parameter is used to access the the device registry only.</span></span> <span data-ttu-id="9190f-110">Bu nedenle ilkenin kayıt defterine okuma erişimi olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9190f-110">Therefore the policy should have read access to the registry.</span></span>
<span data-ttu-id="9190f-111">IoT Hub belirteçleri için ilke SAS 'ın bir parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="9190f-111">For IoT Hub tokens the policy is part of the SAS.</span></span>

## <span data-ttu-id="9190f-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9190f-112">EXAMPLES</span></span>

### <span data-ttu-id="9190f-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9190f-113">Example 1</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="9190f-114">Iothubowner ilkesini ve birincil anahtarı kullanarak IoT merkezi SAS belirteci oluşturun.</span><span class="sxs-lookup"><span data-stu-id="9190f-114">Generate an IoT Hub SAS token using the iothubowner policy and primary key.</span></span>

### <span data-ttu-id="9190f-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="9190f-115">Example 2</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -KeyName "registryRead" -KeyType "secondary"
```

<span data-ttu-id="9190f-116">RegistryRead ilkesini ve ikincil anahtarını kullanarak IoT merkezi SAS belirteci oluşturun.</span><span class="sxs-lookup"><span data-stu-id="9190f-116">Generate an IoT Hub SAS token using the registryRead policy and secondary key.</span></span>

### <span data-ttu-id="9190f-117">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="9190f-117">Example 3</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="9190f-118">{İothub_name} cihaz kayıt defterine erişmek için ıothubowner ilkesini kullanarak bir cihaz SAS belirteci oluşturun.</span><span class="sxs-lookup"><span data-stu-id="9190f-118">Generate a device SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

### <span data-ttu-id="9190f-119">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="9190f-119">Example 4</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="9190f-120">{İothub_name} cihaz kayıt defterine erişmek için ıothubowner ilkesini kullanarak bir modül SAS belirteci oluşturun.</span><span class="sxs-lookup"><span data-stu-id="9190f-120">Generate a module SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

## <span data-ttu-id="9190f-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9190f-121">PARAMETERS</span></span>

### <span data-ttu-id="9190f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9190f-122">-DefaultProfile</span></span>
<span data-ttu-id="9190f-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9190f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9190f-124">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="9190f-124">-DeviceId</span></span>
<span data-ttu-id="9190f-125">Hedef cihaz kimliği.</span><span class="sxs-lookup"><span data-stu-id="9190f-125">Target Device Id.</span></span>

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

### <span data-ttu-id="9190f-126">-Süre</span><span class="sxs-lookup"><span data-stu-id="9190f-126">-Duration</span></span>
<span data-ttu-id="9190f-127">Oluşturulacak belirtecin gelecek süre sonu (saniye).</span><span class="sxs-lookup"><span data-stu-id="9190f-127">Future expiry (in seconds) of the token to be generated.</span></span>
<span data-ttu-id="9190f-128">Varsayılan 3600 ' dır.</span><span class="sxs-lookup"><span data-stu-id="9190f-128">Default is 3600.</span></span>

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

### <span data-ttu-id="9190f-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9190f-129">-InputObject</span></span>
<span data-ttu-id="9190f-130">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="9190f-130">IotHub object</span></span>

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

### <span data-ttu-id="9190f-131">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="9190f-131">-IotHubName</span></span>
<span data-ttu-id="9190f-132">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="9190f-132">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="9190f-133">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="9190f-133">-KeyName</span></span>
<span data-ttu-id="9190f-134">Access anahtar adı.</span><span class="sxs-lookup"><span data-stu-id="9190f-134">Access key name.</span></span>

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

### <span data-ttu-id="9190f-135">-KeyType</span><span class="sxs-lookup"><span data-stu-id="9190f-135">-KeyType</span></span>
<span data-ttu-id="9190f-136">Access anahtar türü.</span><span class="sxs-lookup"><span data-stu-id="9190f-136">Access key type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSKeyType
Parameter Sets: (All)
Aliases:
Accepted values: primary, secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9190f-137">-ModuleID</span><span class="sxs-lookup"><span data-stu-id="9190f-137">-ModuleId</span></span>
<span data-ttu-id="9190f-138">Hedef modül kimliği.</span><span class="sxs-lookup"><span data-stu-id="9190f-138">Target Module Id.</span></span>

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

### <span data-ttu-id="9190f-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9190f-139">-ResourceGroupName</span></span>
<span data-ttu-id="9190f-140">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="9190f-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9190f-141">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9190f-141">-ResourceId</span></span>
<span data-ttu-id="9190f-142">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="9190f-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="9190f-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="9190f-143">-Confirm</span></span>
<span data-ttu-id="9190f-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9190f-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9190f-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9190f-145">-WhatIf</span></span>
<span data-ttu-id="9190f-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9190f-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9190f-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9190f-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9190f-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9190f-148">CommonParameters</span></span>
<span data-ttu-id="9190f-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9190f-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9190f-150">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9190f-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9190f-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9190f-151">INPUTS</span></span>

### <span data-ttu-id="9190f-152">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="9190f-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="9190f-153">System. String</span><span class="sxs-lookup"><span data-stu-id="9190f-153">System.String</span></span>

## <span data-ttu-id="9190f-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9190f-154">OUTPUTS</span></span>

### <span data-ttu-id="9190f-155">System. String</span><span class="sxs-lookup"><span data-stu-id="9190f-155">System.String</span></span>

## <span data-ttu-id="9190f-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9190f-156">NOTES</span></span>

## <span data-ttu-id="9190f-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9190f-157">RELATED LINKS</span></span>
