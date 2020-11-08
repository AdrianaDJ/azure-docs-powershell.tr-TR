---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubJob.md
ms.openlocfilehash: 7c5c09f2379eb1c0306b89018732336b4223f5c9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097371"
---
# <span data-ttu-id="03d14-101">Get-AzIotHubJob</span><span class="sxs-lookup"><span data-stu-id="03d14-101">Get-AzIotHubJob</span></span>

## <span data-ttu-id="03d14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03d14-102">SYNOPSIS</span></span>
<span data-ttu-id="03d14-103">Bir IotHub işi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="03d14-103">Gets the information about an IotHub job.</span></span>

## <span data-ttu-id="03d14-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="03d14-104">SYNTAX</span></span>

```
Get-AzIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03d14-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="03d14-105">DESCRIPTION</span></span>
<span data-ttu-id="03d14-106">Bir IotHub Işi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="03d14-106">Gets the information about an IotHub Job.</span></span>
<span data-ttu-id="03d14-107">New-AzIotHubExportDevices veya New-AzIotHubImportDevices komutları kullanılarak içeri veya dışarı aktarma işlemi başlatıldığında bir IotHub Işi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="03d14-107">An IotHub Job gets created when an import or export operation is initialized using the New-AzIotHubExportDevices or New-AzIotHubImportDevices commands.</span></span>
<span data-ttu-id="03d14-108">Tüm işleri listeleyebilir veya Iş tanımlayıcısına göre işlere filtre uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="03d14-108">You can either list all the jobs or filter the jobs by the Job Identifier.</span></span>

## <span data-ttu-id="03d14-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="03d14-109">EXAMPLES</span></span>

### <span data-ttu-id="03d14-110">Örnek 1 tüm Işleri Listele</span><span class="sxs-lookup"><span data-stu-id="03d14-110">Example 1 List all Jobs</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="03d14-111">"Myiothub" adlı IotHub 'in tüm işlerini alır</span><span class="sxs-lookup"><span data-stu-id="03d14-111">Gets all the jobs for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="03d14-112">Örnek 2 belirli bir Iş edinme</span><span class="sxs-lookup"><span data-stu-id="03d14-112">Example 2 Get a specific Job</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

<span data-ttu-id="03d14-113">"IotHub" adlı için "3630fc31-4caa-43e8-A232-ea0577221cb2" tanımlayıcılı iş hakkında bilgi alır</span><span class="sxs-lookup"><span data-stu-id="03d14-113">Gets information about the job with the identifier "3630fc31-4caa-43e8-a232-ea0577221cb2" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="03d14-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="03d14-114">PARAMETERS</span></span>

### <span data-ttu-id="03d14-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03d14-115">-DefaultProfile</span></span>
<span data-ttu-id="03d14-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="03d14-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="03d14-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="03d14-117">-JobId</span></span>
<span data-ttu-id="03d14-118">Iş tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="03d14-118">The Job Identifier.</span></span> 

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

### <span data-ttu-id="03d14-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="03d14-119">-Name</span></span>
<span data-ttu-id="03d14-120">IoT Hub adı.</span><span class="sxs-lookup"><span data-stu-id="03d14-120">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="03d14-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03d14-121">-ResourceGroupName</span></span>
<span data-ttu-id="03d14-122">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="03d14-122">Resource Group Name</span></span>

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

### <span data-ttu-id="03d14-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03d14-123">CommonParameters</span></span>
<span data-ttu-id="03d14-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="03d14-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03d14-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03d14-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03d14-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="03d14-126">INPUTS</span></span>

### <span data-ttu-id="03d14-127">System. String</span><span class="sxs-lookup"><span data-stu-id="03d14-127">System.String</span></span>

## <span data-ttu-id="03d14-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="03d14-128">OUTPUTS</span></span>

### <span data-ttu-id="03d14-129">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiotubjobresponse</span><span class="sxs-lookup"><span data-stu-id="03d14-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="03d14-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="03d14-130">NOTES</span></span>

## <span data-ttu-id="03d14-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="03d14-131">RELATED LINKS</span></span>
