---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D53DAEB6-DC4F-473C-A193-A1E2A65326D4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: a67113443702d443bfd0b936af05e14c8fbbb96e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588280"
---
# <span data-ttu-id="20a87-101">New-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="20a87-101">New-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="20a87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20a87-102">SYNOPSIS</span></span>
<span data-ttu-id="20a87-103">Bir toplu Iş hesabında bir uygulama paketi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="20a87-103">Creates an application package in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20a87-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="20a87-104">SYNTAX</span></span>

### <span data-ttu-id="20a87-105">Uploadandacyalın (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="20a87-105">UploadAndActivate (Default)</span></span>
```
New-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-Format] <String> -FilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20a87-106">Yalnızca Activate</span><span class="sxs-lookup"><span data-stu-id="20a87-106">ActivateOnly</span></span>
```
New-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-Format] <String> [-ActivateOnly]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20a87-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="20a87-107">DESCRIPTION</span></span>
<span data-ttu-id="20a87-108">**New-AzureRmBatchApplicationPackage** cmdlet 'ı bir Azure Batch hesabında uygulama paketi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="20a87-108">The **New-AzureRmBatchApplicationPackage** cmdlet creates an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="20a87-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="20a87-109">EXAMPLES</span></span>

### <span data-ttu-id="20a87-110">Örnek 1: bir uygulama paketini bir toplu Iş hesabına yükleme</span><span class="sxs-lookup"><span data-stu-id="20a87-110">Example 1: Install an application package into a Batch account</span></span>
```
PS C:\>New-AzureRmBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -ApplicationVersion "1.0" -FilePath "litware.1.0.zip" -Format "zip"
```

<span data-ttu-id="20a87-111">Bu komut, Litwin uygulamasının 1,0 sürümünü oluşturur ve etkinleştirir ve litware.1.0.zip içeriğini uygulama paketi içeriği olarak yükler.</span><span class="sxs-lookup"><span data-stu-id="20a87-111">This command creates and activates version 1.0 of the Litware application, and uploads the contents of litware.1.0.zip as the application package content.</span></span>

## <span data-ttu-id="20a87-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="20a87-112">PARAMETERS</span></span>

### <span data-ttu-id="20a87-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="20a87-113">-AccountName</span></span>
<span data-ttu-id="20a87-114">Bu cmdlet 'in uygulama paketi eklediği toplu Iş hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="20a87-114">Specifies the name of the Batch account to which this cmdlet adds an application package.</span></span>

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

### <span data-ttu-id="20a87-115">-Yalnızca Activate</span><span class="sxs-lookup"><span data-stu-id="20a87-115">-ActivateOnly</span></span>
<span data-ttu-id="20a87-116">Bu cmdlet 'in önceden yüklenmiş bir uygulama paketini etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="20a87-116">Indicates that this cmdlet activates an application package that has already been uploaded.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ActivateOnly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20a87-117">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="20a87-117">-ApplicationId</span></span>
<span data-ttu-id="20a87-118">Uygulamanın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="20a87-118">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="20a87-119">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="20a87-119">-ApplicationVersion</span></span>
<span data-ttu-id="20a87-120">Uygulamanın sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="20a87-120">Specifies the version of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20a87-121">-DosyaYolu</span><span class="sxs-lookup"><span data-stu-id="20a87-121">-FilePath</span></span>
<span data-ttu-id="20a87-122">Uygulama paketi ikili dosyası olarak yüklenecek dosyayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="20a87-122">Specifies the file to be uploaded as the application package binary file.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadAndActivate
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20a87-123">Biçimli</span><span class="sxs-lookup"><span data-stu-id="20a87-123">-Format</span></span>
<span data-ttu-id="20a87-124">Uygulama paketi ikili dosyasının biçimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="20a87-124">Specifies the format of the application package binary file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20a87-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20a87-125">-ResourceGroupName</span></span>
<span data-ttu-id="20a87-126">Toplu Iş hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="20a87-126">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="20a87-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20a87-127">-DefaultProfile</span></span>
<span data-ttu-id="20a87-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="20a87-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20a87-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20a87-129">CommonParameters</span></span>
<span data-ttu-id="20a87-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="20a87-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20a87-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20a87-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20a87-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="20a87-132">INPUTS</span></span>

## <span data-ttu-id="20a87-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="20a87-133">OUTPUTS</span></span>

### <span data-ttu-id="20a87-134">Microsoft.Azure.Commands.Batch. Modeller. PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="20a87-134">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="20a87-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="20a87-135">NOTES</span></span>

## <span data-ttu-id="20a87-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="20a87-136">RELATED LINKS</span></span>

[<span data-ttu-id="20a87-137">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="20a87-137">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="20a87-138">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="20a87-138">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="20a87-139">Yeni-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="20a87-139">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="20a87-140">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="20a87-140">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="20a87-141">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="20a87-141">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="20a87-142">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="20a87-142">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


