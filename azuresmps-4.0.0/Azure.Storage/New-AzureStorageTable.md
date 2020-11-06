---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9a58f869d5308b176a68614cbb2fa2fec401fa14
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572193"
---
# <span data-ttu-id="a3cc6-101">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="a3cc6-101">New-AzureStorageTable</span></span>

## <span data-ttu-id="a3cc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3cc6-102">SYNOPSIS</span></span>
<span data-ttu-id="a3cc6-103">Depolama tablosu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a3cc6-103">Creates a storage table.</span></span>

## <span data-ttu-id="a3cc6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a3cc6-104">SYNTAX</span></span>

```
New-AzureStorageTable [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="a3cc6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a3cc6-105">DESCRIPTION</span></span>
<span data-ttu-id="a3cc6-106">**New-AzureStorageTable** cmdlet 'ı, Azure 'daki depolama hesabıyla ilişkilendirilmiş bir depolama tablosu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a3cc6-106">The **New-AzureStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="a3cc6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a3cc6-107">EXAMPLES</span></span>

### <span data-ttu-id="a3cc6-108">Örnek 1: Azure depolama tablosu oluşturma</span><span class="sxs-lookup"><span data-stu-id="a3cc6-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzureStorageTable -Name "tableabc"
```

<span data-ttu-id="a3cc6-109">Bu komut, tableabc adında bir depolama tablosu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a3cc6-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="a3cc6-110">Örnek 2: birden çok Azure depolama tablosu oluşturma</span><span class="sxs-lookup"><span data-stu-id="a3cc6-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzureStorageTable
```

<span data-ttu-id="a3cc6-111">Bu komut birden çok tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a3cc6-111">This command creates multiple tables.</span></span>
<span data-ttu-id="a3cc6-112">.NET **String** sınıfının **bölme** yöntemini kullanır ve sonra da ardışık düzene geçirir.</span><span class="sxs-lookup"><span data-stu-id="a3cc6-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="a3cc6-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a3cc6-113">PARAMETERS</span></span>

### <span data-ttu-id="a3cc6-114">-Context</span><span class="sxs-lookup"><span data-stu-id="a3cc6-114">-Context</span></span>
<span data-ttu-id="a3cc6-115">Depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3cc6-115">Specifies the storage context.</span></span>
<span data-ttu-id="a3cc6-116">Bunu oluşturmak için New-AzureStorageContext cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a3cc6-116">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a3cc6-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="a3cc6-117">-Name</span></span>
<span data-ttu-id="a3cc6-118">Yeni tablo için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3cc6-118">Specifies a name for the new table.</span></span>

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

### <span data-ttu-id="a3cc6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3cc6-119">CommonParameters</span></span>
<span data-ttu-id="a3cc6-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a3cc6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3cc6-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3cc6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3cc6-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a3cc6-122">INPUTS</span></span>

## <span data-ttu-id="a3cc6-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a3cc6-123">OUTPUTS</span></span>

## <span data-ttu-id="a3cc6-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a3cc6-124">NOTES</span></span>

## <span data-ttu-id="a3cc6-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a3cc6-125">RELATED LINKS</span></span>

[<span data-ttu-id="a3cc6-126">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="a3cc6-126">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)

[<span data-ttu-id="a3cc6-127">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="a3cc6-127">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)


