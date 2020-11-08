---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
ms.openlocfilehash: 3ba9706c452c293dea6ad6a0e23a51ccb03ada9c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097368"
---
# <span data-ttu-id="159e5-101">Update-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="159e5-101">Update-AzIotHub</span></span>

## <span data-ttu-id="159e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="159e5-102">SYNOPSIS</span></span>
<span data-ttu-id="159e5-103">Azure IoT Hub 'ı güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="159e5-103">Update an Azure IoT Hub.</span></span>

## <span data-ttu-id="159e5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="159e5-104">SYNTAX</span></span>

```
Update-AzIotHub -ResourceGroupName <String> -Name <String> -Tag <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="159e5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="159e5-105">DESCRIPTION</span></span>
<span data-ttu-id="159e5-106">Bir IotHub 'in etiket özelliklerini güncelleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="159e5-106">You can update the tags properties of an IotHub.</span></span>

## <span data-ttu-id="159e5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="159e5-107">EXAMPLES</span></span>

### <span data-ttu-id="159e5-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="159e5-108">Example 1</span></span>
```
PS C:\> Update-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag @tags

Id             : /subscriptions/91d1xxxx-xxxx-xxxx-xxxx-xxxxxxxxddc0/resourceGroups/myresourcegroup/providers/Microsoft.De
                 vices/IotHubs/myiotdps
Name           : myiotdps
Type           : Microsoft.Devices/IotHubs
Location       : East US
Tags           : {[k1, v1]}
Properties     : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties
Sku            : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuInfo
```

<span data-ttu-id="159e5-109">" @tags " Öğesini Azure IoT Hub etiketine "myıotdps" etiketine ekleyin.</span><span class="sxs-lookup"><span data-stu-id="159e5-109">Add "@tags" to the Tag of an Azure IoT Hub "myiotdps".</span></span>

## <span data-ttu-id="159e5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="159e5-110">PARAMETERS</span></span>

### <span data-ttu-id="159e5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="159e5-111">-DefaultProfile</span></span>
<span data-ttu-id="159e5-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="159e5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="159e5-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="159e5-113">-Name</span></span>
<span data-ttu-id="159e5-114">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="159e5-114">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="159e5-115">-Reset</span><span class="sxs-lookup"><span data-stu-id="159e5-115">-Reset</span></span>
<span data-ttu-id="159e5-116">IoTHub etiketlerini sıfırlama</span><span class="sxs-lookup"><span data-stu-id="159e5-116">Reset IoTHub Tags</span></span>

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

### <span data-ttu-id="159e5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="159e5-117">-ResourceGroupName</span></span>
<span data-ttu-id="159e5-118">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="159e5-118">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="159e5-119">Etiketli</span><span class="sxs-lookup"><span data-stu-id="159e5-119">-Tag</span></span>
<span data-ttu-id="159e5-120">IoTHub etiket koleksiyonu</span><span class="sxs-lookup"><span data-stu-id="159e5-120">IoTHub Tag collection</span></span>

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

### <span data-ttu-id="159e5-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="159e5-121">-Confirm</span></span>
<span data-ttu-id="159e5-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="159e5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="159e5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="159e5-123">-WhatIf</span></span>
<span data-ttu-id="159e5-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="159e5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="159e5-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="159e5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="159e5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="159e5-126">CommonParameters</span></span>
<span data-ttu-id="159e5-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="159e5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="159e5-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="159e5-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="159e5-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="159e5-129">INPUTS</span></span>

### <span data-ttu-id="159e5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="159e5-130">System.String</span></span>

## <span data-ttu-id="159e5-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="159e5-131">OUTPUTS</span></span>

### <span data-ttu-id="159e5-132">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="159e5-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="159e5-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="159e5-133">NOTES</span></span>

## <span data-ttu-id="159e5-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="159e5-134">RELATED LINKS</span></span>
