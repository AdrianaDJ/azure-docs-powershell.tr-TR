---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmoduleconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
ms.openlocfilehash: 30926eaad6447f109b1755d419be0b3931a76054
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098861"
---
# <span data-ttu-id="f2d99-101">Get-AzIotHubModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="f2d99-101">Get-AzIotHubModuleConnectionString</span></span>

## <span data-ttu-id="f2d99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2d99-102">SYNOPSIS</span></span>
<span data-ttu-id="f2d99-103">Bir IoT Hub 'ında hedef IoT aygıt modülünün bağlantı dizesini edinin.</span><span class="sxs-lookup"><span data-stu-id="f2d99-103">Get the connection string of a target IoT device module in an Iot Hub.</span></span>

## <span data-ttu-id="f2d99-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f2d99-104">SYNTAX</span></span>

### <span data-ttu-id="f2d99-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f2d99-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2d99-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="f2d99-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleConnectionString [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2d99-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="f2d99-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2d99-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f2d99-108">DESCRIPTION</span></span>
<span data-ttu-id="f2d99-109">Tüm modüllerin veya Azure IoT Hub 'ındaki bir hedef IoT aygıtının belirtilen modülünün bağlantı dizesi.</span><span class="sxs-lookup"><span data-stu-id="f2d99-109">List connection string of all modules or a specified module of a target IoT device contained within an Azure IoT Hub.</span></span>

## <span data-ttu-id="f2d99-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f2d99-110">EXAMPLES</span></span>

### <span data-ttu-id="f2d99-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f2d99-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleConnectionString -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Deviceid "myDevice1"

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******     
module2   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module2;x509=true
```

<span data-ttu-id="f2d99-112">Bir IoT merkezi 'nde hedef IoT aygıtının tüm modüller bağlantı dizelerini gösterin.</span><span class="sxs-lookup"><span data-stu-id="f2d99-112">Show all modules connection string of a target IoT device in an Iot Hub.</span></span>

### <span data-ttu-id="f2d99-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="f2d99-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubMCS -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "module1" -KeyType secondary

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******
```

<span data-ttu-id="f2d99-114">Bir IoT Hub 'ında hedef IoT aygıtının ikincil modül bağlantı dizesini edinin.</span><span class="sxs-lookup"><span data-stu-id="f2d99-114">Get the secondary module connection string of a target IoT device in an Iot Hub.</span></span>

## <span data-ttu-id="f2d99-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f2d99-115">PARAMETERS</span></span>

### <span data-ttu-id="f2d99-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2d99-116">-DefaultProfile</span></span>
<span data-ttu-id="f2d99-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f2d99-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2d99-118">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="f2d99-118">-DeviceId</span></span>
<span data-ttu-id="f2d99-119">Hedef cihaz kimliği.</span><span class="sxs-lookup"><span data-stu-id="f2d99-119">Target Device Id.</span></span>

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

### <span data-ttu-id="f2d99-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2d99-120">-InputObject</span></span>
<span data-ttu-id="f2d99-121">IotHub nesnesi</span><span class="sxs-lookup"><span data-stu-id="f2d99-121">IotHub object</span></span>

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

### <span data-ttu-id="f2d99-122">-Iothubname</span><span class="sxs-lookup"><span data-stu-id="f2d99-122">-IotHubName</span></span>
<span data-ttu-id="f2d99-123">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="f2d99-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="f2d99-124">-KeyType</span><span class="sxs-lookup"><span data-stu-id="f2d99-124">-KeyType</span></span>
<span data-ttu-id="f2d99-125">Kimlik doğrulama için paylaşılan erişim ilkesi anahtarı türü.</span><span class="sxs-lookup"><span data-stu-id="f2d99-125">Shared access policy key type for auth.</span></span>

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

### <span data-ttu-id="f2d99-126">-ModuleID</span><span class="sxs-lookup"><span data-stu-id="f2d99-126">-ModuleId</span></span>
<span data-ttu-id="f2d99-127">Hedef modül kimliği.</span><span class="sxs-lookup"><span data-stu-id="f2d99-127">Target Module Id.</span></span>

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

### <span data-ttu-id="f2d99-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2d99-128">-ResourceGroupName</span></span>
<span data-ttu-id="f2d99-129">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="f2d99-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f2d99-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f2d99-130">-ResourceId</span></span>
<span data-ttu-id="f2d99-131">IotHub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="f2d99-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="f2d99-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2d99-132">CommonParameters</span></span>
<span data-ttu-id="f2d99-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f2d99-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2d99-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2d99-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2d99-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f2d99-135">INPUTS</span></span>

### <span data-ttu-id="f2d99-136">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="f2d99-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="f2d99-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f2d99-137">System.String</span></span>

## <span data-ttu-id="f2d99-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f2d99-138">OUTPUTS</span></span>

### <span data-ttu-id="f2d99-139">Microsoft. Azure. Commands. Management. IotHub. modeller. PSModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="f2d99-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleConnectionString</span></span>

## <span data-ttu-id="f2d99-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f2d99-140">NOTES</span></span>

## <span data-ttu-id="f2d99-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f2d99-141">RELATED LINKS</span></span>
