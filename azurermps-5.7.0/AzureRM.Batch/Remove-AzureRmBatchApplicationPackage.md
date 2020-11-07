---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FD2E3442-9CEA-4390-BE9C-772C7D6FD1E2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurermbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: 0ae0003c4c38b7e3922694ed01f6d8f4d10a49d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764724"
---
# <span data-ttu-id="9119e-101">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="9119e-101">Remove-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="9119e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9119e-102">SYNOPSIS</span></span>
<span data-ttu-id="9119e-103">Uygulama paketi kaydını ve ikili dosyayı siler.</span><span class="sxs-lookup"><span data-stu-id="9119e-103">Deletes an application package record and the binary file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9119e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9119e-104">SYNTAX</span></span>

```
Remove-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9119e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9119e-105">DESCRIPTION</span></span>
<span data-ttu-id="9119e-106">**Remove-AzureRmBatchApplicationPackage** cmdlet 'i bir uygulama paketi kaydını ve bir Azure toplu hesabındaki ikili dosyayı siler.</span><span class="sxs-lookup"><span data-stu-id="9119e-106">The **Remove-AzureRmBatchApplicationPackage** cmdlet deletes an application package record and the binary file from an Azure Batch account.</span></span>

## <span data-ttu-id="9119e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9119e-107">EXAMPLES</span></span>

### <span data-ttu-id="9119e-108">Örnek 1: bir uygulama paketini toplu hesaptan silme</span><span class="sxs-lookup"><span data-stu-id="9119e-108">Example 1: Delete an application package from a Batch account</span></span>
```
PS C:\>Remove-AzureRmBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "litware" -ApplicationVersion "1.0"
```

<span data-ttu-id="9119e-109">Bu komut, ContosoBatchGroup hesabındaki Litwin uygulamasının 1,0 sürümünü siler.</span><span class="sxs-lookup"><span data-stu-id="9119e-109">This command deletes version 1.0 of the Litware application from the ContosoBatchGroup account.</span></span>
<span data-ttu-id="9119e-110">Komut hem paket kaydını hem de paket ikili dosyasını içeren blobu siler.</span><span class="sxs-lookup"><span data-stu-id="9119e-110">The command deletes both the package record and the blob that contain the package binary file.</span></span>

## <span data-ttu-id="9119e-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9119e-111">PARAMETERS</span></span>

### <span data-ttu-id="9119e-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9119e-112">-AccountName</span></span>
<span data-ttu-id="9119e-113">Bu cmdlet 'in uygulama paketini sildiği toplu Iş hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9119e-113">Specifies the name of the Batch account from which this cmdlet deletes an application package.</span></span>

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

### <span data-ttu-id="9119e-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="9119e-114">-ApplicationId</span></span>
<span data-ttu-id="9119e-115">Uygulamanın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="9119e-115">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="9119e-116">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="9119e-116">-ApplicationVersion</span></span>
<span data-ttu-id="9119e-117">Uygulamanın sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="9119e-117">Specifies the version of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9119e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9119e-118">-DefaultProfile</span></span>
<span data-ttu-id="9119e-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9119e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9119e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9119e-120">-ResourceGroupName</span></span>
<span data-ttu-id="9119e-121">Toplu Iş hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9119e-121">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="9119e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9119e-122">CommonParameters</span></span>
<span data-ttu-id="9119e-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9119e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9119e-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9119e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9119e-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9119e-125">INPUTS</span></span>

### <span data-ttu-id="9119e-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9119e-126">None</span></span>
<span data-ttu-id="9119e-127">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="9119e-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9119e-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9119e-128">OUTPUTS</span></span>

## <span data-ttu-id="9119e-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9119e-129">NOTES</span></span>

## <span data-ttu-id="9119e-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9119e-130">RELATED LINKS</span></span>

[<span data-ttu-id="9119e-131">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="9119e-131">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="9119e-132">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="9119e-132">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="9119e-133">Yeni-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="9119e-133">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="9119e-134">Yeni-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="9119e-134">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="9119e-135">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="9119e-135">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="9119e-136">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="9119e-136">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


