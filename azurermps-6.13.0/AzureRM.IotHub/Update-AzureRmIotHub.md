---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/update-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Update-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Update-AzureRmIotHub.md
ms.openlocfilehash: 6a71c2318a709eb8d4b3fe2fe68a760919097aca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594020"
---
# <span data-ttu-id="66563-101">Update-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="66563-101">Update-AzureRmIotHub</span></span>

## <span data-ttu-id="66563-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66563-102">SYNOPSIS</span></span>
<span data-ttu-id="66563-103">Azure IoT Hub 'ı güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="66563-103">Update an Azure IoT Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66563-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="66563-104">SYNTAX</span></span>

```
Update-AzureRmIotHub -ResourceGroupName <String> -Name <String> -Tag <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66563-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="66563-105">DESCRIPTION</span></span>
<span data-ttu-id="66563-106">Bir IotHub 'in etiket özelliklerini güncelleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="66563-106">You can update the tags properties of an IotHub.</span></span>

## <span data-ttu-id="66563-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="66563-107">EXAMPLES</span></span>

### <span data-ttu-id="66563-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="66563-108">Example 1</span></span>
```
PS C:\> Update-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag @tags

Id             : /subscriptions/91d1xxxx-xxxx-xxxx-xxxx-xxxxxxxxddc0/resourceGroups/myresourcegroup/providers/Microsoft.De
                 vices/IotHubs/myiotdps
Name           : myiotdps
Type           : Microsoft.Devices/IotHubs
Location       : East US
Tags           : {[k1, v1]}
Properties     : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties
Sku            : Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuInfo
```

<span data-ttu-id="66563-109">" @tags " Öğesini Azure IoT Hub etiketine "myıotdps" etiketine ekleyin.</span><span class="sxs-lookup"><span data-stu-id="66563-109">Add "@tags" to the Tag of an Azure IoT Hub "myiotdps".</span></span>

## <span data-ttu-id="66563-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="66563-110">PARAMETERS</span></span>

### <span data-ttu-id="66563-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66563-111">-DefaultProfile</span></span>
<span data-ttu-id="66563-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="66563-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66563-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="66563-113">-Name</span></span>
<span data-ttu-id="66563-114">IoT Hub adı</span><span class="sxs-lookup"><span data-stu-id="66563-114">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="66563-115">-Reset</span><span class="sxs-lookup"><span data-stu-id="66563-115">-Reset</span></span>
<span data-ttu-id="66563-116">IoTHub etiketlerini sıfırlama</span><span class="sxs-lookup"><span data-stu-id="66563-116">Reset IoTHub Tags</span></span>

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

### <span data-ttu-id="66563-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66563-117">-ResourceGroupName</span></span>
<span data-ttu-id="66563-118">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="66563-118">Name of the Resource Group</span></span>

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

### <span data-ttu-id="66563-119">Etiketli</span><span class="sxs-lookup"><span data-stu-id="66563-119">-Tag</span></span>
<span data-ttu-id="66563-120">IoTHub etiket koleksiyonu</span><span class="sxs-lookup"><span data-stu-id="66563-120">IoTHub Tag collection</span></span>

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

### <span data-ttu-id="66563-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="66563-121">-Confirm</span></span>
<span data-ttu-id="66563-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="66563-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66563-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66563-123">-WhatIf</span></span>
<span data-ttu-id="66563-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="66563-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66563-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="66563-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66563-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66563-126">CommonParameters</span></span>
<span data-ttu-id="66563-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="66563-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66563-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66563-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66563-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="66563-129">INPUTS</span></span>

### <span data-ttu-id="66563-130">System. String</span><span class="sxs-lookup"><span data-stu-id="66563-130">System.String</span></span>

## <span data-ttu-id="66563-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="66563-131">OUTPUTS</span></span>

### <span data-ttu-id="66563-132">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="66563-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="66563-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="66563-133">NOTES</span></span>

## <span data-ttu-id="66563-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="66563-134">RELATED LINKS</span></span>
