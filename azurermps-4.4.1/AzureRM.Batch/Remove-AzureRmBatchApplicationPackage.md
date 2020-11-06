---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FD2E3442-9CEA-4390-BE9C-772C7D6FD1E2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: 8ef7ba1c678c09ba10bd87c301a417600f51fe0c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591805"
---
# <span data-ttu-id="128c1-101">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="128c1-101">Remove-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="128c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="128c1-102">SYNOPSIS</span></span>
<span data-ttu-id="128c1-103">Uygulama paketi kaydını ve ikili dosyayı siler.</span><span class="sxs-lookup"><span data-stu-id="128c1-103">Deletes an application package record and the binary file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="128c1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="128c1-104">SYNTAX</span></span>

```
Remove-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="128c1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="128c1-105">DESCRIPTION</span></span>
<span data-ttu-id="128c1-106">**Remove-AzureRmBatchApplicationPackage** cmdlet 'i bir uygulama paketi kaydını ve bir Azure toplu hesabındaki ikili dosyayı siler.</span><span class="sxs-lookup"><span data-stu-id="128c1-106">The **Remove-AzureRmBatchApplicationPackage** cmdlet deletes an application package record and the binary file from an Azure Batch account.</span></span>

## <span data-ttu-id="128c1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="128c1-107">EXAMPLES</span></span>

### <span data-ttu-id="128c1-108">Örnek 1: bir uygulama paketini toplu hesaptan silme</span><span class="sxs-lookup"><span data-stu-id="128c1-108">Example 1: Delete an application package from a Batch account</span></span>
```
PS C:\>Remove-AzureRmBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "litware" -ApplicationVersion "1.0"
```

<span data-ttu-id="128c1-109">Bu komut, ContosoBatchGroup hesabındaki Litwin uygulamasının 1,0 sürümünü siler.</span><span class="sxs-lookup"><span data-stu-id="128c1-109">This command deletes version 1.0 of the Litware application from the ContosoBatchGroup account.</span></span>
<span data-ttu-id="128c1-110">Komut hem paket kaydını hem de paket ikili dosyasını içeren blobu siler.</span><span class="sxs-lookup"><span data-stu-id="128c1-110">The command deletes both the package record and the blob that contain the package binary file.</span></span>

## <span data-ttu-id="128c1-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="128c1-111">PARAMETERS</span></span>

### <span data-ttu-id="128c1-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="128c1-112">-AccountName</span></span>
<span data-ttu-id="128c1-113">Bu cmdlet 'in uygulama paketini sildiği toplu Iş hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="128c1-113">Specifies the name of the Batch account from which this cmdlet deletes an application package.</span></span>

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

### <span data-ttu-id="128c1-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="128c1-114">-ApplicationId</span></span>
<span data-ttu-id="128c1-115">Uygulamanın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="128c1-115">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="128c1-116">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="128c1-116">-ApplicationVersion</span></span>
<span data-ttu-id="128c1-117">Uygulamanın sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="128c1-117">Specifies the version of the application.</span></span>

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

### <span data-ttu-id="128c1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="128c1-118">-ResourceGroupName</span></span>
<span data-ttu-id="128c1-119">Toplu Iş hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="128c1-119">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="128c1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="128c1-120">-DefaultProfile</span></span>
<span data-ttu-id="128c1-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="128c1-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="128c1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="128c1-122">CommonParameters</span></span>
<span data-ttu-id="128c1-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="128c1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="128c1-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="128c1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="128c1-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="128c1-125">INPUTS</span></span>

## <span data-ttu-id="128c1-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="128c1-126">OUTPUTS</span></span>

## <span data-ttu-id="128c1-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="128c1-127">NOTES</span></span>

## <span data-ttu-id="128c1-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="128c1-128">RELATED LINKS</span></span>

[<span data-ttu-id="128c1-129">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="128c1-129">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="128c1-130">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="128c1-130">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="128c1-131">Yeni-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="128c1-131">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="128c1-132">Yeni-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="128c1-132">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="128c1-133">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="128c1-133">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="128c1-134">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="128c1-134">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


