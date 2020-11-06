---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/new-azurermiothubimportdevices
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubImportDevices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubImportDevices.md
ms.openlocfilehash: 84b8224c83e6455e7f59b8a5fe2b330f34e61ac5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589770"
---
# <span data-ttu-id="3250a-101">New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="3250a-101">New-AzureRmIotHubImportDevices</span></span>

## <span data-ttu-id="3250a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3250a-102">SYNOPSIS</span></span>
<span data-ttu-id="3250a-103">Yeni bir cihaz içeri aktarma işi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3250a-103">Creates a new import devices job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3250a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3250a-104">SYNTAX</span></span>

```
New-AzureRmIotHubImportDevices [-ResourceGroupName] <String> [-Name] <String> [-InputBlobContainerUri] <String>
 [-OutputBlobContainerUri] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3250a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3250a-105">DESCRIPTION</span></span>
<span data-ttu-id="3250a-106">IotHub için yeni bir aygıt içeri aktarma işi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3250a-106">Creates a new import devices job for the IotHub.</span></span>
<span data-ttu-id="3250a-107">Bu, tüm cihazları belirtilen kapsayıcıdan IotHub içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="3250a-107">This will import all the devices to the IotHub from the specified container.</span></span> <span data-ttu-id="3250a-108">SAS URI 'sini oluşturma konusunda aşağıdaki makaleye bakın.</span><span class="sxs-lookup"><span data-stu-id="3250a-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="3250a-109"> https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span><span class="sxs-lookup"><span data-stu-id="3250a-109">https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span></span>

## <span data-ttu-id="3250a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3250a-110">EXAMPLES</span></span>

### <span data-ttu-id="3250a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3250a-111">Example 1</span></span>
```
PS C:\> New-AzureRmIotHubImportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

<span data-ttu-id="3250a-112">IotHub "myiothub" için yeni bir aygıt alma isteği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3250a-112">Creates a new import device request for the IotHub "myiothub".</span></span>

## <span data-ttu-id="3250a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3250a-113">PARAMETERS</span></span>

### <span data-ttu-id="3250a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3250a-114">-DefaultProfile</span></span>
<span data-ttu-id="3250a-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3250a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3250a-116">-Inputblobcontaineruri</span><span class="sxs-lookup"><span data-stu-id="3250a-116">-InputBlobContainerUri</span></span>
<span data-ttu-id="3250a-117">FileUpload için giriş blob kapsayıcı URI 'Si</span><span class="sxs-lookup"><span data-stu-id="3250a-117">Input Blob Container Uri for FileUpload</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3250a-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="3250a-118">-Name</span></span>
<span data-ttu-id="3250a-119">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="3250a-119">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3250a-120">-OutputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="3250a-120">-OutputBlobContainerUri</span></span>
<span data-ttu-id="3250a-121">Çıktının yazılacağı URI.</span><span class="sxs-lookup"><span data-stu-id="3250a-121">The Uri to write the output to.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3250a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3250a-122">-ResourceGroupName</span></span>
<span data-ttu-id="3250a-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="3250a-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3250a-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="3250a-124">-Confirm</span></span>
<span data-ttu-id="3250a-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3250a-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3250a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3250a-126">-WhatIf</span></span>
<span data-ttu-id="3250a-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3250a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3250a-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3250a-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3250a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3250a-129">CommonParameters</span></span>
<span data-ttu-id="3250a-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3250a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3250a-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3250a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3250a-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3250a-132">INPUTS</span></span>

### <span data-ttu-id="3250a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3250a-133">System.String</span></span>

## <span data-ttu-id="3250a-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3250a-134">OUTPUTS</span></span>

### <span data-ttu-id="3250a-135">Microsoft. Azure. Management. IotHub. modeller. JobResponse</span><span class="sxs-lookup"><span data-stu-id="3250a-135">Microsoft.Azure.Management.IotHub.Models.JobResponse</span></span>

## <span data-ttu-id="3250a-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3250a-136">NOTES</span></span>

## <span data-ttu-id="3250a-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3250a-137">RELATED LINKS</span></span>

