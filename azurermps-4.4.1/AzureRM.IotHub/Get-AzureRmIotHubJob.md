---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubJob.md
ms.openlocfilehash: b0ea6f3cae3fe978a3d24b055eb47693ea466272
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763726"
---
# <span data-ttu-id="2e09d-101">Get-AzureRmIotHubJob</span><span class="sxs-lookup"><span data-stu-id="2e09d-101">Get-AzureRmIotHubJob</span></span>

## <span data-ttu-id="2e09d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e09d-102">SYNOPSIS</span></span>
<span data-ttu-id="2e09d-103">Bir IotHub işi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="2e09d-103">Gets the information about an IotHub job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e09d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2e09d-104">SYNTAX</span></span>

```
Get-AzureRmIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e09d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2e09d-105">DESCRIPTION</span></span>
<span data-ttu-id="2e09d-106">Bir IotHub Işi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="2e09d-106">Gets the information about an IotHub Job.</span></span>
<span data-ttu-id="2e09d-107">Bir IotHub Işi, içeri veya dışarı aktarma işlemi başlatıldığında New-AzureRmIotHubExportDevices veya New-AzureRmIotHubImportDevices komutları kullanılarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2e09d-107">An IotHub Job gets created when an import or export operation is initialted using the New-AzureRmIotHubExportDevices or New-AzureRmIotHubImportDevices commands.</span></span>
<span data-ttu-id="2e09d-108">Tüm işleri listeleyebilir veya Iş tanımlayıcısına göre işlere filtre uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2e09d-108">You can either list all the jobs or filter the jobs by the Job Identifier.</span></span>

## <span data-ttu-id="2e09d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2e09d-109">EXAMPLES</span></span>

### <span data-ttu-id="2e09d-110">Örnek 1 tüm Işleri Listele</span><span class="sxs-lookup"><span data-stu-id="2e09d-110">Example 1 List all Jobs</span></span>
```
PS C:\> Get-AzureRmIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="2e09d-111">"Myiothub" adlı IotHub 'in tüm işlerini alır</span><span class="sxs-lookup"><span data-stu-id="2e09d-111">Gets all the jobs for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="2e09d-112">Örnek 2 belirli bir Iş edinme</span><span class="sxs-lookup"><span data-stu-id="2e09d-112">Example 2 Get a specific Job</span></span>
```
PS C:\> Get-AzureRmIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

<span data-ttu-id="2e09d-113">"IotHub" adlı için "3630fc31-4caa-43e8-A232-ea0577221cb2" tanımlayıcılı iş hakkında bilgi alır</span><span class="sxs-lookup"><span data-stu-id="2e09d-113">Gets information about the job with the identifier "3630fc31-4caa-43e8-a232-ea0577221cb2" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="2e09d-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2e09d-114">PARAMETERS</span></span>

### <span data-ttu-id="2e09d-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="2e09d-115">-JobId</span></span>
<span data-ttu-id="2e09d-116">Iş tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="2e09d-116">The Job Identifier.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e09d-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="2e09d-117">-Name</span></span>
<span data-ttu-id="2e09d-118">IoT Hub adı.</span><span class="sxs-lookup"><span data-stu-id="2e09d-118">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="2e09d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e09d-119">-ResourceGroupName</span></span>
<span data-ttu-id="2e09d-120">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="2e09d-120">Resource Group Name</span></span>

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

### <span data-ttu-id="2e09d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e09d-121">-DefaultProfile</span></span>
<span data-ttu-id="2e09d-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2e09d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e09d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e09d-123">CommonParameters</span></span>
<span data-ttu-id="2e09d-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2e09d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e09d-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e09d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e09d-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2e09d-126">INPUTS</span></span>

### <span data-ttu-id="2e09d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="2e09d-127">System.String</span></span>

## <span data-ttu-id="2e09d-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2e09d-128">OUTPUTS</span></span>

### <span data-ttu-id="2e09d-129">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiotubjobresponse</span><span class="sxs-lookup"><span data-stu-id="2e09d-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>
<span data-ttu-id="2e09d-130">System. topluluklar. Generic. LIST \` 1 \[ \[ Microsoft. Azure. Commands. Management. IotHub. modeller. Psiotubjobresponse, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="2e09d-130">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="2e09d-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2e09d-131">NOTES</span></span>

## <span data-ttu-id="2e09d-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2e09d-132">RELATED LINKS</span></span>

