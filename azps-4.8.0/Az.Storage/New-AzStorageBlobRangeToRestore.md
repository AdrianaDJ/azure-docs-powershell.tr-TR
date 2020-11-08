---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: cfbe2cc695ceb2db7c498e8ee2750fa0427da114
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273799"
---
# <span data-ttu-id="0456e-101">New-AzStorageBlobRangeToRestore</span><span class="sxs-lookup"><span data-stu-id="0456e-101">New-AzStorageBlobRangeToRestore</span></span>

## <span data-ttu-id="0456e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0456e-102">SYNOPSIS</span></span>
<span data-ttu-id="0456e-103">Depolama hesabını geri yüklemek için blob Aralık nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0456e-103">Creates a Blob Range object to restores a Storage account.</span></span>

## <span data-ttu-id="0456e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0456e-104">SYNTAX</span></span>

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0456e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0456e-105">DESCRIPTION</span></span>
<span data-ttu-id="0456e-106">**Yeni-AzStorageBlobRangeToRestore** cmdlet 'i restore-AzStorageBlobRange 'de kullanılabilen bir blob Aralık nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0456e-106">The **New-AzStorageBlobRangeToRestore** cmdlet creates a Blob range object, which can be used in Restore-AzStorageBlobRange.</span></span>

## <span data-ttu-id="0456e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0456e-107">EXAMPLES</span></span>

### <span data-ttu-id="0456e-108">Örnek 1: geri yüklenecek blob aralığı oluşturur</span><span class="sxs-lookup"><span data-stu-id="0456e-108">Example 1: Creates a blob range to restore</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

<span data-ttu-id="0456e-109">Bu komut geri yüklemek için container1/blob1 (Include) ve Container2/blob2 (exclude) ile biten bir blob aralığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0456e-109">This command creates a blob range to restore, which starts at container1/blob1 (include), and ends at container2/blob2 (exclude).</span></span>

### <span data-ttu-id="0456e-110">Örnek 2: ilk Blobun ilk blob 'dan belirli bir blob 'a geri yüklenecek bir blob aralığı oluşturur (Dışla)</span><span class="sxs-lookup"><span data-stu-id="0456e-110">Example 2: Creates a blob range which will restore from first blob in alphabetical order, to a specific blob (exclude)</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

<span data-ttu-id="0456e-111">Bu komut, alfabetik sıranın ilk blosonra belirli bir blob container2/blob2 (hariç tut) geri yüklenecek bir blob aralığı oluşturur</span><span class="sxs-lookup"><span data-stu-id="0456e-111">This command creates a blob range which will restore from first blob of alphabetical order, to a specific blob container2/blob2 (exclude)</span></span>

### <span data-ttu-id="0456e-112">Örnek 3: belirli bir Blobun (Include) en son blob 'u alfabetik sırada geri yüklenecek bir blob aralığı oluşturur</span><span class="sxs-lookup"><span data-stu-id="0456e-112">Example 3: Creates a blob range which will restore from a specific blob (include), to the last blob in alphabetical order</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

<span data-ttu-id="0456e-113">Bu komut, belirli bir blob container1/blob1 (include) en son blob 'a alfabetik sırada geri yüklenecek bir blob aralığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0456e-113">This command creates a blob range which will restore from a specific blob container1/blob1 (include), to the last blob in alphabetical order.</span></span>

### <span data-ttu-id="0456e-114">Örnek 4: tüm blob 'ları geri yüklenecek blob aralığı oluşturur</span><span class="sxs-lookup"><span data-stu-id="0456e-114">Example 4: Creates a blob range which will restore all blobs</span></span>
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

<span data-ttu-id="0456e-115">Bu komut, tüm blob 'ları geri yüklenecek blob aralığı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0456e-115">This command creates a blob range which will restore all blobs.</span></span>

## <span data-ttu-id="0456e-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0456e-116">PARAMETERS</span></span>

### <span data-ttu-id="0456e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0456e-117">-DefaultProfile</span></span>
<span data-ttu-id="0456e-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0456e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0456e-119">-EndRange</span><span class="sxs-lookup"><span data-stu-id="0456e-119">-EndRange</span></span>
<span data-ttu-id="0456e-120">Blob geri yükleme bitiş aralığını belirtin.</span><span class="sxs-lookup"><span data-stu-id="0456e-120">Specify the blob restore End range.</span></span>
<span data-ttu-id="0456e-121">Son Aralık geri yükleme bloblarını dışarıda bırakılacak.</span><span class="sxs-lookup"><span data-stu-id="0456e-121">End range will be excluded in restore blobs.</span></span>
<span data-ttu-id="0456e-122">Sonuna geri dönmek için boş bir stri olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="0456e-122">Set it as empty strng to restore to the end.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0456e-123">-StartRange</span><span class="sxs-lookup"><span data-stu-id="0456e-123">-StartRange</span></span>
<span data-ttu-id="0456e-124">Blob geri yükleme başlangıç aralığını belirtin.</span><span class="sxs-lookup"><span data-stu-id="0456e-124">Specify the blob restore start range.</span></span>
<span data-ttu-id="0456e-125">Başlangıç aralığı geri yükleme bloblarını içerir.</span><span class="sxs-lookup"><span data-stu-id="0456e-125">Start range will be included in restore blobs.</span></span>
<span data-ttu-id="0456e-126">Başlangıçtan geri yüklemek için boş dize olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="0456e-126">Set it as empty string to restore from begining.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0456e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0456e-127">CommonParameters</span></span>
<span data-ttu-id="0456e-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0456e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0456e-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0456e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0456e-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0456e-130">INPUTS</span></span>

### <span data-ttu-id="0456e-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0456e-131">None</span></span>

## <span data-ttu-id="0456e-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0456e-132">OUTPUTS</span></span>

### <span data-ttu-id="0456e-133">Microsoft. Azure. Commands. Management. Storage. model. PSBlobRestoreRange</span><span class="sxs-lookup"><span data-stu-id="0456e-133">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange</span></span>

## <span data-ttu-id="0456e-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0456e-134">NOTES</span></span>

## <span data-ttu-id="0456e-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0456e-135">RELATED LINKS</span></span>
