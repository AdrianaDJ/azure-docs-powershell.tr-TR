---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FF111B74-90A3-4F7C-B515-CE1EEF68EB54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurermbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplication.md
ms.openlocfilehash: 77b3d446c52e72bc31a2802768b00822982d1ea2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764185"
---
# <span data-ttu-id="722df-101">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="722df-101">New-AzureRmBatchApplication</span></span>

## <span data-ttu-id="722df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="722df-102">SYNOPSIS</span></span>
<span data-ttu-id="722df-103">Belirtilen toplu hesaba uygulama ekler.</span><span class="sxs-lookup"><span data-stu-id="722df-103">Adds an application to the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="722df-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="722df-104">SYNTAX</span></span>

```
New-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [[-AllowUpdates] <Boolean>] [[-DisplayName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="722df-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="722df-105">DESCRIPTION</span></span>
<span data-ttu-id="722df-106">**New-AzureRmBatchApplication** cmdlet 'ı belirtilen Azure toplu hesabına bir uygulama ekler.</span><span class="sxs-lookup"><span data-stu-id="722df-106">The **New-AzureRmBatchApplication** cmdlet adds an application to the specified Azure Batch account.</span></span>

## <span data-ttu-id="722df-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="722df-107">EXAMPLES</span></span>

### <span data-ttu-id="722df-108">Örnek 1: bir toplu Iş hesabına boş uygulama ekleme</span><span class="sxs-lookup"><span data-stu-id="722df-108">Example 1: Add an empty application to a Batch account</span></span>
```
PS C:\>New-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -AllowUpdates $True -DisplayName "Litware Advanced Reticulator"
```

<span data-ttu-id="722df-109">Bu komut, ContosoBatch hesabında Litwin uygulamasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="722df-109">This command creates the Litware application in the ContosoBatch account.</span></span>
<span data-ttu-id="722df-110">Uygulama başlangıçta paket yok.</span><span class="sxs-lookup"><span data-stu-id="722df-110">The application initially contains no packages.</span></span>

## <span data-ttu-id="722df-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="722df-111">PARAMETERS</span></span>

### <span data-ttu-id="722df-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="722df-112">-AccountName</span></span>
<span data-ttu-id="722df-113">Bu cmdlet 'in uygulama eklediği toplu Iş hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="722df-113">Specifies the name of the Batch account to which this cmdlet adds an application.</span></span>

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

### <span data-ttu-id="722df-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="722df-114">-AllowUpdates</span></span>
<span data-ttu-id="722df-115">Uygulamanın içindeki paketlerin aynı sürüm dizesini kullanarak yazılıp yazılmayacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="722df-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="722df-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="722df-116">-ApplicationId</span></span>
<span data-ttu-id="722df-117">Uygulamanın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="722df-117">Specifies the ID of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="722df-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="722df-118">-DefaultProfile</span></span>
<span data-ttu-id="722df-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="722df-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="722df-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="722df-120">-DisplayName</span></span>
<span data-ttu-id="722df-121">Uygulamanın görünen adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="722df-121">Specifies the display name for the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="722df-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="722df-122">-ResourceGroupName</span></span>
<span data-ttu-id="722df-123">Toplu Iş hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="722df-123">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="722df-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="722df-124">CommonParameters</span></span>
<span data-ttu-id="722df-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="722df-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="722df-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="722df-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="722df-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="722df-127">INPUTS</span></span>

### <span data-ttu-id="722df-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="722df-128">None</span></span>
<span data-ttu-id="722df-129">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="722df-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="722df-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="722df-130">OUTPUTS</span></span>

### <span data-ttu-id="722df-131">Microsoft.Azure.Commands.Batch. Modeller. PSApplication</span><span class="sxs-lookup"><span data-stu-id="722df-131">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="722df-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="722df-132">NOTES</span></span>

## <span data-ttu-id="722df-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="722df-133">RELATED LINKS</span></span>

[<span data-ttu-id="722df-134">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="722df-134">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="722df-135">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="722df-135">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="722df-136">Yeni-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="722df-136">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="722df-137">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="722df-137">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="722df-138">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="722df-138">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="722df-139">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="722df-139">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)

