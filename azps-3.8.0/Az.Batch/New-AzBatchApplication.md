---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FF111B74-90A3-4F7C-B515-CE1EEF68EB54
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplication.md
ms.openlocfilehash: 44d3c44effa74844713f6ecdf3012109f29b61b6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097924"
---
# <span data-ttu-id="f719b-101">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="f719b-101">New-AzBatchApplication</span></span>

## <span data-ttu-id="f719b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f719b-102">SYNOPSIS</span></span>
<span data-ttu-id="f719b-103">Belirtilen toplu hesaba uygulama ekler.</span><span class="sxs-lookup"><span data-stu-id="f719b-103">Adds an application to the specified Batch account.</span></span>

## <span data-ttu-id="f719b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f719b-104">SYNTAX</span></span>

```
New-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [[-AllowUpdates] <Boolean>] [[-DisplayName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f719b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f719b-105">DESCRIPTION</span></span>
<span data-ttu-id="f719b-106">**New-AzBatchApplication** cmdlet 'ı belirtilen Azure toplu hesabına bir uygulama ekler.</span><span class="sxs-lookup"><span data-stu-id="f719b-106">The **New-AzBatchApplication** cmdlet adds an application to the specified Azure Batch account.</span></span>

## <span data-ttu-id="f719b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f719b-107">EXAMPLES</span></span>

### <span data-ttu-id="f719b-108">Örnek 1: bir toplu Iş hesabına boş uygulama ekleme</span><span class="sxs-lookup"><span data-stu-id="f719b-108">Example 1: Add an empty application to a Batch account</span></span>
```
PS C:\>New-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -AllowUpdates $True -DisplayName "Litware Advanced Reticulator"
```

<span data-ttu-id="f719b-109">Bu komut, ContosoBatch hesabında Litwin uygulamasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f719b-109">This command creates the Litware application in the ContosoBatch account.</span></span>
<span data-ttu-id="f719b-110">Uygulama başlangıçta paket yok.</span><span class="sxs-lookup"><span data-stu-id="f719b-110">The application initially contains no packages.</span></span>

## <span data-ttu-id="f719b-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f719b-111">PARAMETERS</span></span>

### <span data-ttu-id="f719b-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f719b-112">-AccountName</span></span>
<span data-ttu-id="f719b-113">Bu cmdlet 'in uygulama eklediği toplu Iş hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f719b-113">Specifies the name of the Batch account to which this cmdlet adds an application.</span></span>

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

### <span data-ttu-id="f719b-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="f719b-114">-AllowUpdates</span></span>
<span data-ttu-id="f719b-115">Uygulamanın içindeki paketlerin aynı sürüm dizesini kullanarak yazılıp yazılmayacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f719b-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

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

### <span data-ttu-id="f719b-116">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="f719b-116">-ApplicationName</span></span>
<span data-ttu-id="f719b-117">Uygulamanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f719b-117">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f719b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f719b-118">-DefaultProfile</span></span>
<span data-ttu-id="f719b-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f719b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f719b-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f719b-120">-DisplayName</span></span>
<span data-ttu-id="f719b-121">Uygulamanın görünen adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f719b-121">Specifies the display name for the application.</span></span>

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

### <span data-ttu-id="f719b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f719b-122">-ResourceGroupName</span></span>
<span data-ttu-id="f719b-123">Toplu Iş hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f719b-123">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="f719b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f719b-124">CommonParameters</span></span>
<span data-ttu-id="f719b-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f719b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f719b-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f719b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f719b-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f719b-127">INPUTS</span></span>

### <span data-ttu-id="f719b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f719b-128">System.String</span></span>

### <span data-ttu-id="f719b-129">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f719b-129">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="f719b-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f719b-130">OUTPUTS</span></span>

### <span data-ttu-id="f719b-131">Microsoft.Azure.Commands.Batch. Modeller. PSApplication</span><span class="sxs-lookup"><span data-stu-id="f719b-131">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="f719b-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f719b-132">NOTES</span></span>

## <span data-ttu-id="f719b-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f719b-133">RELATED LINKS</span></span>

[<span data-ttu-id="f719b-134">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="f719b-134">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="f719b-135">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="f719b-135">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="f719b-136">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="f719b-136">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="f719b-137">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="f719b-137">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="f719b-138">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="f719b-138">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="f719b-139">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="f719b-139">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


