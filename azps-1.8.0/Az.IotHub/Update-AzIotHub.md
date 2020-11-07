---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHub.md
ms.openlocfilehash: 794ee1187043a800c6f847df215ddb288bb9da9e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916391"
---
# <span data-ttu-id="9cb7c-101">Update-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="9cb7c-101">Update-AzIotHub</span></span>

## <span data-ttu-id="9cb7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cb7c-102">SYNOPSIS</span></span>
<span data-ttu-id="9cb7c-103">Azure IoT Hub 'ı güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="9cb7c-103">Update an Azure IoT Hub.</span></span>

## <span data-ttu-id="9cb7c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9cb7c-104">SYNTAX</span></span>

```
Update-AzIotHub -ResourceGroupName <String> -Name <String> -Tag <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cb7c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9cb7c-105">DESCRIPTION</span></span>
<span data-ttu-id="9cb7c-106">Bir IotHub 'in etiket özelliklerini güncelleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9cb7c-106">You can update the tags properties of an IotHub.</span></span>

## <span data-ttu-id="9cb7c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9cb7c-107">EXAMPLES</span></span>

### <span data-ttu-id="9cb7c-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9cb7c-108">Example 1</span></span>
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

<span data-ttu-id="9cb7c-109">" @tags " Öğesini Azure IoT Hub etiketine "myıotdps" etiketine ekleyin.</span><span class="sxs-lookup"><span data-stu-id="9cb7c-109">Add "@tags" to the Tag of an Azure IoT Hub "myiotdps".</span></span>

## <span data-ttu-id="9cb7c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9cb7c-110">PARAMETERS</span></span>

### <span data-ttu-id="9cb7c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cb7c-111">-DefaultProfile</span></span>
<span data-ttu-id="9cb7c-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9cb7c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cb7c-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="9cb7c-113">-Name</span></span>
<span data-ttu-id="9cb7c-114">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="9cb7c-114">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="9cb7c-115">-Reset</span><span class="sxs-lookup"><span data-stu-id="9cb7c-115">-Reset</span></span>
<span data-ttu-id="9cb7c-116">IoTHub etiketlerini sıfırlama</span><span class="sxs-lookup"><span data-stu-id="9cb7c-116">Reset IoTHub Tags</span></span>

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

### <span data-ttu-id="9cb7c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cb7c-117">-ResourceGroupName</span></span>
<span data-ttu-id="9cb7c-118">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="9cb7c-118">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9cb7c-119">Etiketli</span><span class="sxs-lookup"><span data-stu-id="9cb7c-119">-Tag</span></span>
<span data-ttu-id="9cb7c-120">IoTHub etiket koleksiyonu</span><span class="sxs-lookup"><span data-stu-id="9cb7c-120">IoTHub Tag collection</span></span>

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

### <span data-ttu-id="9cb7c-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="9cb7c-121">-Confirm</span></span>
<span data-ttu-id="9cb7c-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9cb7c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cb7c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cb7c-123">-WhatIf</span></span>
<span data-ttu-id="9cb7c-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9cb7c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cb7c-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9cb7c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cb7c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cb7c-126">CommonParameters</span></span>
<span data-ttu-id="9cb7c-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9cb7c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cb7c-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cb7c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cb7c-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9cb7c-129">INPUTS</span></span>

### <span data-ttu-id="9cb7c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9cb7c-130">System.String</span></span>

## <span data-ttu-id="9cb7c-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9cb7c-131">OUTPUTS</span></span>

### <span data-ttu-id="9cb7c-132">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="9cb7c-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="9cb7c-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9cb7c-133">NOTES</span></span>

## <span data-ttu-id="9cb7c-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9cb7c-134">RELATED LINKS</span></span>
