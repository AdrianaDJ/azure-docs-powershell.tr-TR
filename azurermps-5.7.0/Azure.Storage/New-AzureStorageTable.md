---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTable.md
ms.openlocfilehash: 53bb5f3a34cddf9e74bfb9d9c9f1bd1d109d8f6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590557"
---
# <span data-ttu-id="58d7e-101">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="58d7e-101">New-AzureStorageTable</span></span>

## <span data-ttu-id="58d7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58d7e-102">SYNOPSIS</span></span>
<span data-ttu-id="58d7e-103">Depolama tablosu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="58d7e-103">Creates a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58d7e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="58d7e-104">SYNTAX</span></span>

```
New-AzureStorageTable [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="58d7e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="58d7e-105">DESCRIPTION</span></span>
<span data-ttu-id="58d7e-106">**New-AzureStorageTable** cmdlet 'ı, Azure 'daki depolama hesabıyla ilişkilendirilmiş bir depolama tablosu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="58d7e-106">The **New-AzureStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="58d7e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="58d7e-107">EXAMPLES</span></span>

### <span data-ttu-id="58d7e-108">Örnek 1: Azure depolama tablosu oluşturma</span><span class="sxs-lookup"><span data-stu-id="58d7e-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzureStorageTable -Name "tableabc"
```

<span data-ttu-id="58d7e-109">Bu komut, tableabc adında bir depolama tablosu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="58d7e-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="58d7e-110">Örnek 2: birden çok Azure depolama tablosu oluşturma</span><span class="sxs-lookup"><span data-stu-id="58d7e-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzureStorageTable
```

<span data-ttu-id="58d7e-111">Bu komut birden çok tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="58d7e-111">This command creates multiple tables.</span></span>
<span data-ttu-id="58d7e-112">.NET **String** sınıfının **bölme** yöntemini kullanır ve sonra da ardışık düzene geçirir.</span><span class="sxs-lookup"><span data-stu-id="58d7e-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="58d7e-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="58d7e-113">PARAMETERS</span></span>

### <span data-ttu-id="58d7e-114">-Context</span><span class="sxs-lookup"><span data-stu-id="58d7e-114">-Context</span></span>
<span data-ttu-id="58d7e-115">Depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="58d7e-115">Specifies the storage context.</span></span>
<span data-ttu-id="58d7e-116">Bunu oluşturmak için New-AzureStorageContext cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="58d7e-116">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58d7e-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="58d7e-117">-Name</span></span>
<span data-ttu-id="58d7e-118">Yeni tablo için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="58d7e-118">Specifies a name for the new table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58d7e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58d7e-119">CommonParameters</span></span>
<span data-ttu-id="58d7e-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="58d7e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58d7e-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58d7e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58d7e-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="58d7e-122">INPUTS</span></span>

### <span data-ttu-id="58d7e-123">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="58d7e-123">IStorageContext</span></span>

<span data-ttu-id="58d7e-124">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="58d7e-124">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="58d7e-125">Dizisi</span><span class="sxs-lookup"><span data-stu-id="58d7e-125">String</span></span>

<span data-ttu-id="58d7e-126">' Name ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="58d7e-126">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="58d7e-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="58d7e-127">OUTPUTS</span></span>

### <span data-ttu-id="58d7e-128">Microsoft. Windowsazde. Commands. Common. Storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="58d7e-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="58d7e-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="58d7e-129">NOTES</span></span>

## <span data-ttu-id="58d7e-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="58d7e-130">RELATED LINKS</span></span>

[<span data-ttu-id="58d7e-131">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="58d7e-131">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)

[<span data-ttu-id="58d7e-132">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="58d7e-132">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)


