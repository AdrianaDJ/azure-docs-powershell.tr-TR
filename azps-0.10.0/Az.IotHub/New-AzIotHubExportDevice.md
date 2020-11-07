---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubexportdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/New-AzIotHubExportDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/New-AzIotHubExportDevice.md
ms.openlocfilehash: 9c1561330d6cd76c7c2d00efc16d61fe3b387b65
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936691"
---
# <span data-ttu-id="17fc0-101">New-AzIotHubExportDevice</span><span class="sxs-lookup"><span data-stu-id="17fc0-101">New-AzIotHubExportDevice</span></span>

## <span data-ttu-id="17fc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17fc0-102">SYNOPSIS</span></span>
<span data-ttu-id="17fc0-103">Yeni bir dışarı aktarma cihazları işi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="17fc0-103">Creates a new export devices job.</span></span>

## <span data-ttu-id="17fc0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="17fc0-104">SYNTAX</span></span>

```
New-AzIotHubExportDevice [-ResourceGroupName] <String> [-Name] <String> [-ExportBlobContainerUri] <String>
 [-ExcludeKeys] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17fc0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="17fc0-105">DESCRIPTION</span></span>
<span data-ttu-id="17fc0-106">IotHub için yeni bir dışarı aktarma cihazları işi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="17fc0-106">Creates a new export devices job for the IotHub.</span></span>
<span data-ttu-id="17fc0-107">Bu işlem tüm cihazları belirtilen kapsayıcıya aktarır.</span><span class="sxs-lookup"><span data-stu-id="17fc0-107">This will export all the devices to the specified container.</span></span> <span data-ttu-id="17fc0-108">SAS URI 'sini oluşturma konusunda aşağıdaki makaleye bakın.</span><span class="sxs-lookup"><span data-stu-id="17fc0-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="17fc0-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span><span class="sxs-lookup"><span data-stu-id="17fc0-109">https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span></span>

## <span data-ttu-id="17fc0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="17fc0-110">EXAMPLES</span></span>

### <span data-ttu-id="17fc0-111">Örnek 1 gönderme cihazı isteği.</span><span class="sxs-lookup"><span data-stu-id="17fc0-111">Example 1 Issue an export device request.</span></span>
```
PS C:\> New-AzIotHubExportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

<span data-ttu-id="17fc0-112">IotHub "myiothub" için yeni bir dışarı aktarma aygıtı isteği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="17fc0-112">Creates a new export device request for the IotHub "myiothub" excluding the keys.</span></span>

## <span data-ttu-id="17fc0-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="17fc0-113">PARAMETERS</span></span>

### <span data-ttu-id="17fc0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17fc0-114">-DefaultProfile</span></span>
<span data-ttu-id="17fc0-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="17fc0-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17fc0-116">-ExcludeKeys</span><span class="sxs-lookup"><span data-stu-id="17fc0-116">-ExcludeKeys</span></span>
<span data-ttu-id="17fc0-117">Anahtarları olmayan cihazları dışarı aktarmaya olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="17fc0-117">Allows to export devices without keys.</span></span>

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

### <span data-ttu-id="17fc0-118">-ExportBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="17fc0-118">-ExportBlobContainerUri</span></span>
<span data-ttu-id="17fc0-119">Blob 'u dışarı aktarma Uri 'Si.</span><span class="sxs-lookup"><span data-stu-id="17fc0-119">The Uri to export the blob to.</span></span> 

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

### <span data-ttu-id="17fc0-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="17fc0-120">-Name</span></span>
<span data-ttu-id="17fc0-121">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="17fc0-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="17fc0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17fc0-122">-ResourceGroupName</span></span>
<span data-ttu-id="17fc0-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="17fc0-123">Resource Group Name</span></span>

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

### <span data-ttu-id="17fc0-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="17fc0-124">-Confirm</span></span>
<span data-ttu-id="17fc0-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="17fc0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17fc0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17fc0-126">-WhatIf</span></span>
<span data-ttu-id="17fc0-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="17fc0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17fc0-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="17fc0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17fc0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17fc0-129">CommonParameters</span></span>
<span data-ttu-id="17fc0-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="17fc0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17fc0-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17fc0-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17fc0-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="17fc0-132">INPUTS</span></span>

### <span data-ttu-id="17fc0-133">System. String</span><span class="sxs-lookup"><span data-stu-id="17fc0-133">System.String</span></span>

## <span data-ttu-id="17fc0-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="17fc0-134">OUTPUTS</span></span>

### <span data-ttu-id="17fc0-135">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiotubjobresponse</span><span class="sxs-lookup"><span data-stu-id="17fc0-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="17fc0-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="17fc0-136">NOTES</span></span>

## <span data-ttu-id="17fc0-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="17fc0-137">RELATED LINKS</span></span>
