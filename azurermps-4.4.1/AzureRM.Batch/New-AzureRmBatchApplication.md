---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FF111B74-90A3-4F7C-B515-CE1EEF68EB54
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplication.md
ms.openlocfilehash: 6c2ab80f5b9fb38ed2f6399d9f186134f4659edf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591806"
---
# <span data-ttu-id="b68b1-101">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b68b1-101">New-AzureRmBatchApplication</span></span>

## <span data-ttu-id="b68b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b68b1-102">SYNOPSIS</span></span>
<span data-ttu-id="b68b1-103">Belirtilen toplu hesaba uygulama ekler.</span><span class="sxs-lookup"><span data-stu-id="b68b1-103">Adds an application to the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b68b1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b68b1-104">SYNTAX</span></span>

```
New-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [[-AllowUpdates] <Boolean>] [[-DisplayName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b68b1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b68b1-105">DESCRIPTION</span></span>
<span data-ttu-id="b68b1-106">**New-AzureRmBatchApplication** cmdlet 'ı belirtilen Azure toplu hesabına bir uygulama ekler.</span><span class="sxs-lookup"><span data-stu-id="b68b1-106">The **New-AzureRmBatchApplication** cmdlet adds an application to the specified Azure Batch account.</span></span>

## <span data-ttu-id="b68b1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b68b1-107">EXAMPLES</span></span>

### <span data-ttu-id="b68b1-108">Örnek 1: bir toplu Iş hesabına boş uygulama ekleme</span><span class="sxs-lookup"><span data-stu-id="b68b1-108">Example 1: Add an empty application to a Batch account</span></span>
```
PS C:\>New-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -AllowUpdates $True -DisplayName "Litware Advanced Reticulator"
```

<span data-ttu-id="b68b1-109">Bu komut, ContosoBatch hesabında Litwin uygulamasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b68b1-109">This command creates the Litware application in the ContosoBatch account.</span></span>
<span data-ttu-id="b68b1-110">Uygulama başlangıçta paket yok.</span><span class="sxs-lookup"><span data-stu-id="b68b1-110">The application initially contains no packages.</span></span>

## <span data-ttu-id="b68b1-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b68b1-111">PARAMETERS</span></span>

### <span data-ttu-id="b68b1-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b68b1-112">-AccountName</span></span>
<span data-ttu-id="b68b1-113">Bu cmdlet 'in uygulama eklediği toplu Iş hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b68b1-113">Specifies the name of the Batch account to which this cmdlet adds an application.</span></span>

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

### <span data-ttu-id="b68b1-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="b68b1-114">-AllowUpdates</span></span>
<span data-ttu-id="b68b1-115">Uygulamanın içindeki paketlerin aynı sürüm dizesini kullanarak yazılıp yazılmayacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b68b1-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b68b1-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="b68b1-116">-ApplicationId</span></span>
<span data-ttu-id="b68b1-117">Uygulamanın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b68b1-117">Specifies the ID of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b68b1-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b68b1-118">-DisplayName</span></span>
<span data-ttu-id="b68b1-119">Uygulamanın görünen adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b68b1-119">Specifies the display name for the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b68b1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b68b1-120">-ResourceGroupName</span></span>
<span data-ttu-id="b68b1-121">Toplu Iş hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b68b1-121">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="b68b1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b68b1-122">-DefaultProfile</span></span>
<span data-ttu-id="b68b1-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b68b1-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b68b1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b68b1-124">CommonParameters</span></span>
<span data-ttu-id="b68b1-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b68b1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b68b1-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b68b1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b68b1-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b68b1-127">INPUTS</span></span>

## <span data-ttu-id="b68b1-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b68b1-128">OUTPUTS</span></span>

### <span data-ttu-id="b68b1-129">Microsoft.Azure.Commands.Batch. Modeller. PSApplication</span><span class="sxs-lookup"><span data-stu-id="b68b1-129">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="b68b1-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b68b1-130">NOTES</span></span>

## <span data-ttu-id="b68b1-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b68b1-131">RELATED LINKS</span></span>

[<span data-ttu-id="b68b1-132">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b68b1-132">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="b68b1-133">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="b68b1-133">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="b68b1-134">Yeni-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="b68b1-134">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="b68b1-135">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b68b1-135">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="b68b1-136">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="b68b1-136">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="b68b1-137">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b68b1-137">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


