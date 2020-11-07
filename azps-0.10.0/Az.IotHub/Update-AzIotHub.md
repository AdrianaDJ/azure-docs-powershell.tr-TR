---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Update-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Update-AzIotHub.md
ms.openlocfilehash: d1b6c8be02ee246053e5930e37186f2a7480325b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936683"
---
# <span data-ttu-id="203ad-101">Update-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="203ad-101">Update-AzIotHub</span></span>

## <span data-ttu-id="203ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="203ad-102">SYNOPSIS</span></span>
<span data-ttu-id="203ad-103">Azure IoT Hub 'ı güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="203ad-103">Update an Azure IoT Hub.</span></span>

## <span data-ttu-id="203ad-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="203ad-104">SYNTAX</span></span>

```
Update-AzIotHub -ResourceGroupName <String> -Name <String> -Tag <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="203ad-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="203ad-105">DESCRIPTION</span></span>
<span data-ttu-id="203ad-106">Bir IotHub 'in etiket özelliklerini güncelleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="203ad-106">You can update the tags properties of an IotHub.</span></span>

## <span data-ttu-id="203ad-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="203ad-107">EXAMPLES</span></span>

### <span data-ttu-id="203ad-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="203ad-108">Example 1</span></span>
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

<span data-ttu-id="203ad-109">" @tags " Öğesini Azure IoT Hub etiketine "myıotdps" etiketine ekleyin.</span><span class="sxs-lookup"><span data-stu-id="203ad-109">Add "@tags" to the Tag of an Azure IoT Hub "myiotdps".</span></span>

## <span data-ttu-id="203ad-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="203ad-110">PARAMETERS</span></span>

### <span data-ttu-id="203ad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="203ad-111">-DefaultProfile</span></span>
<span data-ttu-id="203ad-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="203ad-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="203ad-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="203ad-113">-Name</span></span>
<span data-ttu-id="203ad-114">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="203ad-114">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="203ad-115">-Reset</span><span class="sxs-lookup"><span data-stu-id="203ad-115">-Reset</span></span>
<span data-ttu-id="203ad-116">IoTHub etiketlerini sıfırlama</span><span class="sxs-lookup"><span data-stu-id="203ad-116">Reset IoTHub Tags</span></span>

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

### <span data-ttu-id="203ad-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="203ad-117">-ResourceGroupName</span></span>
<span data-ttu-id="203ad-118">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="203ad-118">Name of the Resource Group</span></span>

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

### <span data-ttu-id="203ad-119">Etiketli</span><span class="sxs-lookup"><span data-stu-id="203ad-119">-Tag</span></span>
<span data-ttu-id="203ad-120">IoTHub etiket koleksiyonu</span><span class="sxs-lookup"><span data-stu-id="203ad-120">IoTHub Tag collection</span></span>

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

### <span data-ttu-id="203ad-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="203ad-121">-Confirm</span></span>
<span data-ttu-id="203ad-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="203ad-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="203ad-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="203ad-123">-WhatIf</span></span>
<span data-ttu-id="203ad-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="203ad-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="203ad-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="203ad-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="203ad-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="203ad-126">CommonParameters</span></span>
<span data-ttu-id="203ad-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="203ad-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="203ad-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="203ad-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="203ad-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="203ad-129">INPUTS</span></span>

### <span data-ttu-id="203ad-130">System. String</span><span class="sxs-lookup"><span data-stu-id="203ad-130">System.String</span></span>

## <span data-ttu-id="203ad-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="203ad-131">OUTPUTS</span></span>

### <span data-ttu-id="203ad-132">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="203ad-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="203ad-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="203ad-133">NOTES</span></span>

## <span data-ttu-id="203ad-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="203ad-134">RELATED LINKS</span></span>
