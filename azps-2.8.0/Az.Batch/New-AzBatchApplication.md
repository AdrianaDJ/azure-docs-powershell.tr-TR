---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FF111B74-90A3-4F7C-B515-CE1EEF68EB54
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplication.md
ms.openlocfilehash: 0c1d847045cc4fb8be39674c13c38114ee9d3a57
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753173"
---
# <span data-ttu-id="d8238-101">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d8238-101">New-AzBatchApplication</span></span>

## <span data-ttu-id="d8238-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8238-102">SYNOPSIS</span></span>
<span data-ttu-id="d8238-103">Belirtilen toplu hesaba uygulama ekler.</span><span class="sxs-lookup"><span data-stu-id="d8238-103">Adds an application to the specified Batch account.</span></span>

## <span data-ttu-id="d8238-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d8238-104">SYNTAX</span></span>

```
New-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [[-AllowUpdates] <Boolean>] [[-DisplayName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d8238-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d8238-105">DESCRIPTION</span></span>
<span data-ttu-id="d8238-106">**New-AzBatchApplication** cmdlet 'ı belirtilen Azure toplu hesabına bir uygulama ekler.</span><span class="sxs-lookup"><span data-stu-id="d8238-106">The **New-AzBatchApplication** cmdlet adds an application to the specified Azure Batch account.</span></span>

## <span data-ttu-id="d8238-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d8238-107">EXAMPLES</span></span>

### <span data-ttu-id="d8238-108">Örnek 1: bir toplu Iş hesabına boş uygulama ekleme</span><span class="sxs-lookup"><span data-stu-id="d8238-108">Example 1: Add an empty application to a Batch account</span></span>
```
PS C:\>New-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -AllowUpdates $True -DisplayName "Litware Advanced Reticulator"
```

<span data-ttu-id="d8238-109">Bu komut, ContosoBatch hesabında Litwin uygulamasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d8238-109">This command creates the Litware application in the ContosoBatch account.</span></span>
<span data-ttu-id="d8238-110">Uygulama başlangıçta paket yok.</span><span class="sxs-lookup"><span data-stu-id="d8238-110">The application initially contains no packages.</span></span>

## <span data-ttu-id="d8238-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d8238-111">PARAMETERS</span></span>

### <span data-ttu-id="d8238-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d8238-112">-AccountName</span></span>
<span data-ttu-id="d8238-113">Bu cmdlet 'in uygulama eklediği toplu Iş hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8238-113">Specifies the name of the Batch account to which this cmdlet adds an application.</span></span>

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

### <span data-ttu-id="d8238-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="d8238-114">-AllowUpdates</span></span>
<span data-ttu-id="d8238-115">Uygulamanın içindeki paketlerin aynı sürüm dizesini kullanarak yazılıp yazılmayacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8238-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

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

### <span data-ttu-id="d8238-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d8238-116">-ApplicationId</span></span>
<span data-ttu-id="d8238-117">Uygulamanın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8238-117">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="d8238-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8238-118">-DefaultProfile</span></span>
<span data-ttu-id="d8238-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d8238-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8238-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d8238-120">-DisplayName</span></span>
<span data-ttu-id="d8238-121">Uygulamanın görünen adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8238-121">Specifies the display name for the application.</span></span>

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

### <span data-ttu-id="d8238-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8238-122">-ResourceGroupName</span></span>
<span data-ttu-id="d8238-123">Toplu Iş hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8238-123">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="d8238-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8238-124">CommonParameters</span></span>
<span data-ttu-id="d8238-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d8238-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8238-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8238-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8238-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d8238-127">INPUTS</span></span>

### <span data-ttu-id="d8238-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d8238-128">System.String</span></span>

### <span data-ttu-id="d8238-129">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="d8238-129">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d8238-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d8238-130">OUTPUTS</span></span>

### <span data-ttu-id="d8238-131">Microsoft.Azure.Commands.Batch. Modeller. PSApplication</span><span class="sxs-lookup"><span data-stu-id="d8238-131">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="d8238-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d8238-132">NOTES</span></span>

## <span data-ttu-id="d8238-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d8238-133">RELATED LINKS</span></span>

[<span data-ttu-id="d8238-134">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d8238-134">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="d8238-135">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d8238-135">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="d8238-136">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d8238-136">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="d8238-137">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d8238-137">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="d8238-138">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d8238-138">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="d8238-139">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d8238-139">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)

