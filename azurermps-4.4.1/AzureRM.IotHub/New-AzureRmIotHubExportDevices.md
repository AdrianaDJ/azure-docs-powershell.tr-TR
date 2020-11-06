---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubExportDevices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubExportDevices.md
ms.openlocfilehash: 3191f4e451ec010a3918130142d08da6f08b3990
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594268"
---
# <span data-ttu-id="bee21-101">New-AzureRmIotHubExportDevices</span><span class="sxs-lookup"><span data-stu-id="bee21-101">New-AzureRmIotHubExportDevices</span></span>

## <span data-ttu-id="bee21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bee21-102">SYNOPSIS</span></span>
<span data-ttu-id="bee21-103">Yeni bir dışarı aktarma cihazları işi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bee21-103">Creates a new export devices job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bee21-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bee21-104">SYNTAX</span></span>

```
New-AzureRmIotHubExportDevices [-ResourceGroupName] <String> [-Name] <String>
 [-ExportBlobContainerUri] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bee21-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bee21-105">DESCRIPTION</span></span>
<span data-ttu-id="bee21-106">IotHub için yeni bir dışarı aktarma cihazları işi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bee21-106">Creates a new export devices job for the IotHub.</span></span>
<span data-ttu-id="bee21-107">Bu işlem tüm cihazları belirtilen kapsayıcıya aktarır.</span><span class="sxs-lookup"><span data-stu-id="bee21-107">This will export all the devices to the specified container.</span></span> <span data-ttu-id="bee21-108">SAS URI 'sini oluşturma konusunda aşağıdaki makaleye bakın.</span><span class="sxs-lookup"><span data-stu-id="bee21-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="bee21-109"> https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span><span class="sxs-lookup"><span data-stu-id="bee21-109">https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span></span>

## <span data-ttu-id="bee21-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bee21-110">EXAMPLES</span></span>

### <span data-ttu-id="bee21-111">Örnek 1 gönderme cihazı isteği.</span><span class="sxs-lookup"><span data-stu-id="bee21-111">Example 1 Issue an export device request.</span></span>
```
PS C:\> New-AzureRmIotHubExportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys $true
```

<span data-ttu-id="bee21-112">IotHub "myiothub" için yeni bir dışarı aktarma aygıtı isteği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bee21-112">Creates a new export device request for the IotHub "myiothub" excluding the keys.</span></span>

## <span data-ttu-id="bee21-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bee21-113">PARAMETERS</span></span>

### <span data-ttu-id="bee21-114">-ExportBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="bee21-114">-ExportBlobContainerUri</span></span>
<span data-ttu-id="bee21-115">Blob 'u dışarı aktarma Uri 'Si.</span><span class="sxs-lookup"><span data-stu-id="bee21-115">The Uri to export the blob to.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bee21-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="bee21-116">-Name</span></span>
<span data-ttu-id="bee21-117">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="bee21-117">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bee21-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bee21-118">-ResourceGroupName</span></span>
<span data-ttu-id="bee21-119">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="bee21-119">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bee21-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="bee21-120">-Confirm</span></span>
<span data-ttu-id="bee21-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bee21-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bee21-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bee21-122">-WhatIf</span></span>
<span data-ttu-id="bee21-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bee21-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bee21-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bee21-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bee21-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bee21-125">-DefaultProfile</span></span>
<span data-ttu-id="bee21-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bee21-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bee21-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bee21-127">CommonParameters</span></span>
<span data-ttu-id="bee21-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bee21-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bee21-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bee21-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bee21-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bee21-130">INPUTS</span></span>

### <span data-ttu-id="bee21-131">System. String</span><span class="sxs-lookup"><span data-stu-id="bee21-131">System.String</span></span>

## <span data-ttu-id="bee21-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bee21-132">OUTPUTS</span></span>

### <span data-ttu-id="bee21-133">Microsoft. Azure. Management. IotHub. modeller. JobResponse</span><span class="sxs-lookup"><span data-stu-id="bee21-133">Microsoft.Azure.Management.IotHub.Models.JobResponse</span></span>

## <span data-ttu-id="bee21-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bee21-134">NOTES</span></span>

## <span data-ttu-id="bee21-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bee21-135">RELATED LINKS</span></span>

