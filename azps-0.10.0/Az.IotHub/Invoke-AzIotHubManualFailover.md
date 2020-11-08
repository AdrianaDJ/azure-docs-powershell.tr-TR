---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmanualfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
ms.openlocfilehash: 5055960ae541ef93d57eee53078413143fad7839
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936700"
---
# <span data-ttu-id="4a5de-101">Invoke-AzIotHubManualFailover</span><span class="sxs-lookup"><span data-stu-id="4a5de-101">Invoke-AzIotHubManualFailover</span></span>

## <span data-ttu-id="4a5de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a5de-102">SYNOPSIS</span></span>
<span data-ttu-id="4a5de-103">IoT Hub 'ı coğrafi olarak eşdeğerli olağanüstü durum kurtarma bölgesine yönelik yük devretme işlemini çağırın.</span><span class="sxs-lookup"><span data-stu-id="4a5de-103">Invoke failover process for the IoT Hub to the geo-paired disaster recovery region.</span></span>

## <span data-ttu-id="4a5de-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4a5de-104">SYNTAX</span></span>

### <span data-ttu-id="4a5de-105">ResourceSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4a5de-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a5de-106">Inputobjectset</span><span class="sxs-lookup"><span data-stu-id="4a5de-106">InputObjectSet</span></span>
```
Invoke-AzIotHubManualFailover [-InputObject] <PSIotHub> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a5de-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="4a5de-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a5de-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4a5de-108">DESCRIPTION</span></span>
<span data-ttu-id="4a5de-109">IoT Hub 'ınızı ikincil konuma tetikler.</span><span class="sxs-lookup"><span data-stu-id="4a5de-109">It will trigger the failover your IoT hub to the secondary location.</span></span> <span data-ttu-id="4a5de-110">Bu eylem, çözümünüze zaman ve telemetri kaybını sağlayacaktır.</span><span class="sxs-lookup"><span data-stu-id="4a5de-110">This action will cause down time and telemetry loss to your solution.</span></span> <span data-ttu-id="4a5de-111">Bu, uzun süren bir işlemdir ve tamamlanması birkaç dakika sürebilir.</span><span class="sxs-lookup"><span data-stu-id="4a5de-111">This is a long running operation and could take several minutes to finish.</span></span> <span data-ttu-id="4a5de-112">Lütfen kullanırken dikkatli olun.</span><span class="sxs-lookup"><span data-stu-id="4a5de-112">Please exercise with caution when using it.</span></span>

## <span data-ttu-id="4a5de-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4a5de-113">EXAMPLES</span></span>

### <span data-ttu-id="4a5de-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4a5de-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="4a5de-115">"Myiothub" IoT Hub 'ın yük devretme işlemi başlatılıyor.</span><span class="sxs-lookup"><span data-stu-id="4a5de-115">Initiating failover process of "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="4a5de-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="4a5de-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub" -AsJob
```

<span data-ttu-id="4a5de-117">Arka planda "myiothub" IoT Hub 'ın yük devretme işlemi başlatılıyor.</span><span class="sxs-lookup"><span data-stu-id="4a5de-117">Initiating failover process of "myiothub" IoT Hub in the background.</span></span>

## <span data-ttu-id="4a5de-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4a5de-118">PARAMETERS</span></span>

### <span data-ttu-id="4a5de-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="4a5de-119">-AsJob</span></span>
<span data-ttu-id="4a5de-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="4a5de-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4a5de-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a5de-121">-DefaultProfile</span></span>
<span data-ttu-id="4a5de-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4a5de-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a5de-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a5de-123">-InputObject</span></span>
<span data-ttu-id="4a5de-124">IoT Hub nesnesi</span><span class="sxs-lookup"><span data-stu-id="4a5de-124">Iot Hub Object</span></span>

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

### <span data-ttu-id="4a5de-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="4a5de-125">-Name</span></span>
<span data-ttu-id="4a5de-126">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="4a5de-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="4a5de-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4a5de-127">-PassThru</span></span>
<span data-ttu-id="4a5de-128">Boole nesnesini döndürmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="4a5de-128">Allows to return the boolean object.</span></span> <span data-ttu-id="4a5de-129">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="4a5de-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4a5de-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a5de-130">-ResourceGroupName</span></span>
<span data-ttu-id="4a5de-131">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="4a5de-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4a5de-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4a5de-132">-ResourceId</span></span>
<span data-ttu-id="4a5de-133">IoT Hub kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="4a5de-133">Iot Hub Resource Id</span></span>

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

### <span data-ttu-id="4a5de-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="4a5de-134">-Confirm</span></span>
<span data-ttu-id="4a5de-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4a5de-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a5de-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a5de-136">-WhatIf</span></span>
<span data-ttu-id="4a5de-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4a5de-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4a5de-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4a5de-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a5de-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a5de-139">CommonParameters</span></span>
<span data-ttu-id="4a5de-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4a5de-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a5de-141">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a5de-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a5de-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4a5de-142">INPUTS</span></span>

### <span data-ttu-id="4a5de-143">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="4a5de-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="4a5de-144">System. String</span><span class="sxs-lookup"><span data-stu-id="4a5de-144">System.String</span></span>

## <span data-ttu-id="4a5de-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4a5de-145">OUTPUTS</span></span>

### <span data-ttu-id="4a5de-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4a5de-146">System.Boolean</span></span>

## <span data-ttu-id="4a5de-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4a5de-147">NOTES</span></span>

## <span data-ttu-id="4a5de-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4a5de-148">RELATED LINKS</span></span>