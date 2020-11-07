---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubimportdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubImportDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubImportDevice.md
ms.openlocfilehash: 2fb9949ecdef64423c6cc074b43f8b58a2ff9e60
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751735"
---
# <span data-ttu-id="fce32-101">New-AzIotHubImportDevice</span><span class="sxs-lookup"><span data-stu-id="fce32-101">New-AzIotHubImportDevice</span></span>

## <span data-ttu-id="fce32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fce32-102">SYNOPSIS</span></span>
<span data-ttu-id="fce32-103">Yeni bir cihaz içeri aktarma işi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fce32-103">Creates a new import devices job.</span></span>

## <span data-ttu-id="fce32-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fce32-104">SYNTAX</span></span>

```
New-AzIotHubImportDevice [-ResourceGroupName] <String> [-Name] <String> [-InputBlobContainerUri] <String>
 [-OutputBlobContainerUri] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fce32-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fce32-105">DESCRIPTION</span></span>
<span data-ttu-id="fce32-106">IotHub için yeni bir aygıt içeri aktarma işi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fce32-106">Creates a new import devices job for the IotHub.</span></span>
<span data-ttu-id="fce32-107">Bu, tüm cihazları belirtilen kapsayıcıdan IotHub içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="fce32-107">This will import all the devices to the IotHub from the specified container.</span></span> <span data-ttu-id="fce32-108">SAS URI 'sini oluşturma konusunda aşağıdaki makaleye bakın.</span><span class="sxs-lookup"><span data-stu-id="fce32-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="fce32-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span><span class="sxs-lookup"><span data-stu-id="fce32-109">https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span></span>

## <span data-ttu-id="fce32-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fce32-110">EXAMPLES</span></span>

### <span data-ttu-id="fce32-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fce32-111">Example 1</span></span>
```
PS C:\> New-AzIotHubImportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

<span data-ttu-id="fce32-112">IotHub "myiothub" için yeni bir aygıt alma isteği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fce32-112">Creates a new import device request for the IotHub "myiothub".</span></span>

## <span data-ttu-id="fce32-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fce32-113">PARAMETERS</span></span>

### <span data-ttu-id="fce32-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fce32-114">-DefaultProfile</span></span>
<span data-ttu-id="fce32-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fce32-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fce32-116">-Inputblobcontaineruri</span><span class="sxs-lookup"><span data-stu-id="fce32-116">-InputBlobContainerUri</span></span>
<span data-ttu-id="fce32-117">FileUpload için giriş blob kapsayıcı URI 'Si</span><span class="sxs-lookup"><span data-stu-id="fce32-117">Input Blob Container Uri for FileUpload</span></span>

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

### <span data-ttu-id="fce32-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="fce32-118">-Name</span></span>
<span data-ttu-id="fce32-119">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="fce32-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="fce32-120">-OutputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="fce32-120">-OutputBlobContainerUri</span></span>
<span data-ttu-id="fce32-121">Çıktının yazılacağı URI.</span><span class="sxs-lookup"><span data-stu-id="fce32-121">The Uri to write the output to.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fce32-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fce32-122">-ResourceGroupName</span></span>
<span data-ttu-id="fce32-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="fce32-123">Resource Group Name</span></span>

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

### <span data-ttu-id="fce32-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="fce32-124">-Confirm</span></span>
<span data-ttu-id="fce32-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fce32-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fce32-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fce32-126">-WhatIf</span></span>
<span data-ttu-id="fce32-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fce32-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fce32-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fce32-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fce32-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fce32-129">CommonParameters</span></span>
<span data-ttu-id="fce32-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fce32-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fce32-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fce32-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fce32-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fce32-132">INPUTS</span></span>

### <span data-ttu-id="fce32-133">System. String</span><span class="sxs-lookup"><span data-stu-id="fce32-133">System.String</span></span>

## <span data-ttu-id="fce32-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fce32-134">OUTPUTS</span></span>

### <span data-ttu-id="fce32-135">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiotubjobresponse</span><span class="sxs-lookup"><span data-stu-id="fce32-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="fce32-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fce32-136">NOTES</span></span>

## <span data-ttu-id="fce32-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fce32-137">RELATED LINKS</span></span>