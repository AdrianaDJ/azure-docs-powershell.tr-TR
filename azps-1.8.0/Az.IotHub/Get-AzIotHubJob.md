---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubJob.md
ms.openlocfilehash: a9218b2e8c03c9b81bad0e1f9723822a09642714
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916472"
---
# <span data-ttu-id="d8e72-101">Get-AzIotHubJob</span><span class="sxs-lookup"><span data-stu-id="d8e72-101">Get-AzIotHubJob</span></span>

## <span data-ttu-id="d8e72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8e72-102">SYNOPSIS</span></span>
<span data-ttu-id="d8e72-103">Bir IotHub işi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="d8e72-103">Gets the information about an IotHub job.</span></span>

## <span data-ttu-id="d8e72-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d8e72-104">SYNTAX</span></span>

```
Get-AzIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8e72-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d8e72-105">DESCRIPTION</span></span>
<span data-ttu-id="d8e72-106">Bir IotHub Işi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="d8e72-106">Gets the information about an IotHub Job.</span></span>
<span data-ttu-id="d8e72-107">Bir IotHub Işi, içeri veya dışarı aktarma işlemi başlatıldığında New-AzIotHubExportDevices veya New-AzIotHubImportDevices komutları kullanılarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="d8e72-107">An IotHub Job gets created when an import or export operation is initialted using the New-AzIotHubExportDevices or New-AzIotHubImportDevices commands.</span></span>
<span data-ttu-id="d8e72-108">Tüm işleri listeleyebilir veya Iş tanımlayıcısına göre işlere filtre uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d8e72-108">You can either list all the jobs or filter the jobs by the Job Identifier.</span></span>

## <span data-ttu-id="d8e72-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d8e72-109">EXAMPLES</span></span>

### <span data-ttu-id="d8e72-110">Örnek 1 tüm Işleri Listele</span><span class="sxs-lookup"><span data-stu-id="d8e72-110">Example 1 List all Jobs</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="d8e72-111">"Myiothub" adlı IotHub 'in tüm işlerini alır</span><span class="sxs-lookup"><span data-stu-id="d8e72-111">Gets all the jobs for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="d8e72-112">Örnek 2 belirli bir Iş edinme</span><span class="sxs-lookup"><span data-stu-id="d8e72-112">Example 2 Get a specific Job</span></span>
```
PS C:\> Get-AzIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

<span data-ttu-id="d8e72-113">"IotHub" adlı için "3630fc31-4caa-43e8-A232-ea0577221cb2" tanımlayıcılı iş hakkında bilgi alır</span><span class="sxs-lookup"><span data-stu-id="d8e72-113">Gets information about the job with the identifier "3630fc31-4caa-43e8-a232-ea0577221cb2" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="d8e72-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d8e72-114">PARAMETERS</span></span>

### <span data-ttu-id="d8e72-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8e72-115">-DefaultProfile</span></span>
<span data-ttu-id="d8e72-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d8e72-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8e72-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="d8e72-117">-JobId</span></span>
<span data-ttu-id="d8e72-118">Iş tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="d8e72-118">The Job Identifier.</span></span> 

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

### <span data-ttu-id="d8e72-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="d8e72-119">-Name</span></span>
<span data-ttu-id="d8e72-120">IoT Hub adı.</span><span class="sxs-lookup"><span data-stu-id="d8e72-120">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="d8e72-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8e72-121">-ResourceGroupName</span></span>
<span data-ttu-id="d8e72-122">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="d8e72-122">Resource Group Name</span></span>

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

### <span data-ttu-id="d8e72-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8e72-123">CommonParameters</span></span>
<span data-ttu-id="d8e72-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d8e72-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8e72-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8e72-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8e72-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d8e72-126">INPUTS</span></span>

### <span data-ttu-id="d8e72-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d8e72-127">System.String</span></span>

## <span data-ttu-id="d8e72-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d8e72-128">OUTPUTS</span></span>

### <span data-ttu-id="d8e72-129">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiotubjobresponse</span><span class="sxs-lookup"><span data-stu-id="d8e72-129">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="d8e72-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d8e72-130">NOTES</span></span>

## <span data-ttu-id="d8e72-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d8e72-131">RELATED LINKS</span></span>