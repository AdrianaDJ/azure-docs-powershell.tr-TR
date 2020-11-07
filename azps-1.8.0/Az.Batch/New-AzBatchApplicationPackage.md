---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D53DAEB6-DC4F-473C-A193-A1E2A65326D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplicationPackage.md
ms.openlocfilehash: 0e5494506873917be7897c547eca900174f5bcab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761462"
---
# <span data-ttu-id="55a1b-101">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="55a1b-101">New-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="55a1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55a1b-102">SYNOPSIS</span></span>
<span data-ttu-id="55a1b-103">Bir toplu Iş hesabında bir uygulama paketi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="55a1b-103">Creates an application package in a Batch account.</span></span>

## <span data-ttu-id="55a1b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="55a1b-104">SYNTAX</span></span>

### <span data-ttu-id="55a1b-105">Uploadandacyalın (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="55a1b-105">UploadAndActivate (Default)</span></span>
```
New-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [-ApplicationVersion] <String> [-Format] <String> -FilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55a1b-106">Yalnızca Activate</span><span class="sxs-lookup"><span data-stu-id="55a1b-106">ActivateOnly</span></span>
```
New-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [-ApplicationVersion] <String> [-Format] <String> [-ActivateOnly] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="55a1b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="55a1b-107">DESCRIPTION</span></span>
<span data-ttu-id="55a1b-108">**New-AzBatchApplicationPackage** cmdlet 'ı bir Azure Batch hesabında uygulama paketi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="55a1b-108">The **New-AzBatchApplicationPackage** cmdlet creates an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="55a1b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="55a1b-109">EXAMPLES</span></span>

### <span data-ttu-id="55a1b-110">Örnek 1: bir uygulama paketini bir toplu Iş hesabına yükleme</span><span class="sxs-lookup"><span data-stu-id="55a1b-110">Example 1: Install an application package into a Batch account</span></span>
```
PS C:\>New-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -ApplicationVersion "1.0" -FilePath "litware.1.0.zip" -Format "zip"
```

<span data-ttu-id="55a1b-111">Bu komut, Litwin uygulamasının 1,0 sürümünü oluşturur ve etkinleştirir ve litware.1.0.zip içeriğini uygulama paketi içeriği olarak yükler.</span><span class="sxs-lookup"><span data-stu-id="55a1b-111">This command creates and activates version 1.0 of the Litware application, and uploads the contents of litware.1.0.zip as the application package content.</span></span>

## <span data-ttu-id="55a1b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="55a1b-112">PARAMETERS</span></span>

### <span data-ttu-id="55a1b-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="55a1b-113">-AccountName</span></span>
<span data-ttu-id="55a1b-114">Bu cmdlet 'in uygulama paketi eklediği toplu Iş hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="55a1b-114">Specifies the name of the Batch account to which this cmdlet adds an application package.</span></span>

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

### <span data-ttu-id="55a1b-115">-Yalnızca Activate</span><span class="sxs-lookup"><span data-stu-id="55a1b-115">-ActivateOnly</span></span>
<span data-ttu-id="55a1b-116">Bu cmdlet 'in önceden yüklenmiş bir uygulama paketini etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="55a1b-116">Indicates that this cmdlet activates an application package that has already been uploaded.</span></span>

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

### <span data-ttu-id="55a1b-117">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="55a1b-117">-ApplicationId</span></span>
<span data-ttu-id="55a1b-118">Uygulamanın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="55a1b-118">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="55a1b-119">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="55a1b-119">-ApplicationVersion</span></span>
<span data-ttu-id="55a1b-120">Uygulamanın sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="55a1b-120">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="55a1b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55a1b-121">-DefaultProfile</span></span>
<span data-ttu-id="55a1b-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="55a1b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55a1b-123">-DosyaYolu</span><span class="sxs-lookup"><span data-stu-id="55a1b-123">-FilePath</span></span>
<span data-ttu-id="55a1b-124">Uygulama paketi ikili dosyası olarak yüklenecek dosyayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="55a1b-124">Specifies the file to be uploaded as the application package binary file.</span></span>

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

### <span data-ttu-id="55a1b-125">Biçimli</span><span class="sxs-lookup"><span data-stu-id="55a1b-125">-Format</span></span>
<span data-ttu-id="55a1b-126">Uygulama paketi ikili dosyasının biçimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="55a1b-126">Specifies the format of the application package binary file.</span></span>

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

### <span data-ttu-id="55a1b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55a1b-127">-ResourceGroupName</span></span>
<span data-ttu-id="55a1b-128">Toplu Iş hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="55a1b-128">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="55a1b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55a1b-129">CommonParameters</span></span>
<span data-ttu-id="55a1b-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="55a1b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55a1b-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55a1b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55a1b-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="55a1b-132">INPUTS</span></span>

### <span data-ttu-id="55a1b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="55a1b-133">System.String</span></span>

### <span data-ttu-id="55a1b-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="55a1b-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="55a1b-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="55a1b-135">OUTPUTS</span></span>

### <span data-ttu-id="55a1b-136">Microsoft.Azure.Commands.Batch. Modeller. PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="55a1b-136">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="55a1b-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="55a1b-137">NOTES</span></span>

## <span data-ttu-id="55a1b-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="55a1b-138">RELATED LINKS</span></span>

[<span data-ttu-id="55a1b-139">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="55a1b-139">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="55a1b-140">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="55a1b-140">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="55a1b-141">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="55a1b-141">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="55a1b-142">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="55a1b-142">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="55a1b-143">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="55a1b-143">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="55a1b-144">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="55a1b-144">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


