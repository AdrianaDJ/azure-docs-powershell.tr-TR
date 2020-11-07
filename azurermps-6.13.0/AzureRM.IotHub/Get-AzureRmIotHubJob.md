---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubJob.md
ms.openlocfilehash: 684b892d2c2cc995e12ae6327541f13428da270f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764396"
---
# <span data-ttu-id="48678-101">Get-AzureRmIotHubJob</span><span class="sxs-lookup"><span data-stu-id="48678-101">Get-AzureRmIotHubJob</span></span>

## <span data-ttu-id="48678-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48678-102">SYNOPSIS</span></span>
<span data-ttu-id="48678-103">Bir IotHub işi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="48678-103">Gets the information about an IotHub job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48678-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="48678-104">SYNTAX</span></span>

```
Get-AzureRmIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48678-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="48678-105">DESCRIPTION</span></span>
<span data-ttu-id="48678-106">Bir IotHub Işi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="48678-106">Gets the information about an IotHub Job.</span></span>
<span data-ttu-id="48678-107">Bir IotHub Işi, içeri veya dışarı aktarma işlemi başlatıldığında New-AzureRmIotHubExportDevices veya New-AzureRmIotHubImportDevices komutları kullanılarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="48678-107">An IotHub Job gets created when an import or export operation is initialted using the New-AzureRmIotHubExportDevices or New-AzureRmIotHubImportDevices commands.</span></span>
<span data-ttu-id="48678-108">Tüm işleri listeleyebilir veya Iş tanımlayıcısına göre işlere filtre uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="48678-108">You can either list all the jobs or filter the jobs by the Job Identifier.</span></span>

## <span data-ttu-id="48678-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="48678-109">EXAMPLES</span></span>

### <span data-ttu-id="48678-110">Örnek 1 tüm Işleri Listele</span><span class="sxs-lookup"><span data-stu-id="48678-110">Example 1 List all Jobs</span></span>
```
PS C:\> Get-AzureRmIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="48678-111">"Myiothub" adlı IotHub 'in tüm işlerini alır</span><span class="sxs-lookup"><span data-stu-id="48678-111">Gets all the jobs for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="48678-112">Örnek 2 belirli bir Iş edinme</span><span class="sxs-lookup"><span data-stu-id="48678-112">Example 2 Get a specific Job</span></span>
```
PS C:\> Get-AzureRmIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

<span data-ttu-id="48678-113">"IotHub" adlı için "3630fc31-4caa-43e8-A232-ea0577221cb2" tanımlayıcılı iş hakkında bilgi alır</span><span class="sxs-lookup"><span data-stu-id="48678-113">Gets information about the job with the identifier "3630fc31-4caa-43e8-a232-ea0577221cb2" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="48678-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="48678-114">PARAMETERS</span></span>

### <span data-ttu-id="48678-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48678-115">-DefaultProfile</span></span>
<span data-ttu-id="48678-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="48678-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48678-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="48678-117">-JobId</span></span>
<span data-ttu-id="48678-118">Iş tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="48678-118">The Job Identifier.</span></span> 

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

### <span data-ttu-id="48678-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="48678-119">-Name</span></span>
<span data-ttu-id="48678-120">IoT Hub adı.</span><span class="sxs-lookup"><span data-stu-id="48678-120">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="48678-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48678-121">-ResourceGroupName</span></span>
<span data-ttu-id="48678-122">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="48678-122">Resource Group Name</span></span>

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

### <span data-ttu-id="48678-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48678-123">CommonParameters</span></span>
<span data-ttu-id="48678-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="48678-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48678-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48678-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48678-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="48678-126">INPUTS</span></span>

### <span data-ttu-id="48678-127">System. String</span><span class="sxs-lookup"><span data-stu-id="48678-127">System.String</span></span>

## <span data-ttu-id="48678-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="48678-128">OUTPUTS</span></span>

### <span data-ttu-id="48678-129">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiotubjobresponse</span><span class="sxs-lookup"><span data-stu-id="48678-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="48678-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="48678-130">NOTES</span></span>

## <span data-ttu-id="48678-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="48678-131">RELATED LINKS</span></span>
