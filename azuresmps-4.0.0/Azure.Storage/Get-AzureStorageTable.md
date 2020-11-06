---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f2bccab190fc27b5e97ecf3af502d3488f28998
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572342"
---
# <span data-ttu-id="d9732-101">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="d9732-101">Get-AzureStorageTable</span></span>

## <span data-ttu-id="d9732-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9732-102">SYNOPSIS</span></span>
<span data-ttu-id="d9732-103">Depolama tablolarını listeler.</span><span class="sxs-lookup"><span data-stu-id="d9732-103">Lists the storage tables.</span></span>

## <span data-ttu-id="d9732-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d9732-104">SYNTAX</span></span>

### <span data-ttu-id="d9732-105">TableName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d9732-105">TableName (Default)</span></span>
```
Get-AzureStorageTable [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="d9732-106">TablePrefix</span><span class="sxs-lookup"><span data-stu-id="d9732-106">TablePrefix</span></span>
```
Get-AzureStorageTable -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="d9732-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d9732-107">DESCRIPTION</span></span>
<span data-ttu-id="d9732-108">**Get-AzureStorageTable** cmdlet 'ı, Azure 'daki depolama hesabıyla ilişkilendirilmiş depolama tablolarını listeler.</span><span class="sxs-lookup"><span data-stu-id="d9732-108">The **Get-AzureStorageTable** cmdlet lists the storage tables associated with the storage account in Azure.</span></span>

## <span data-ttu-id="d9732-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d9732-109">EXAMPLES</span></span>

### <span data-ttu-id="d9732-110">Örnek 1: tüm Azure depolama tablolarını listeler</span><span class="sxs-lookup"><span data-stu-id="d9732-110">Example 1: List all Azure Storage tables</span></span>
```
PS C:\>Get-AzureStorageTable
```

<span data-ttu-id="d9732-111">Bu komut, depolama hesabının tüm depolama tablolarını alır.</span><span class="sxs-lookup"><span data-stu-id="d9732-111">This command gets all storage tables for a Storage account.</span></span>

### <span data-ttu-id="d9732-112">Örnek 2: joker karakter kullanarak Azure depolama tablolarını listeleme</span><span class="sxs-lookup"><span data-stu-id="d9732-112">Example 2: List Azure Storage tables using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageTable -Name table*
```

<span data-ttu-id="d9732-113">Bu komut, adı tabloyla başlayan depolama tablolarını almak için joker karakter kullanır.</span><span class="sxs-lookup"><span data-stu-id="d9732-113">This command uses a wildcard character to get storage tables whose name starts with table.</span></span>

### <span data-ttu-id="d9732-114">Örnek 3: tablo adı önekini kullanarak Azure depolama tablolarını listeleme</span><span class="sxs-lookup"><span data-stu-id="d9732-114">Example 3: List Azure Storage tables using table name prefix</span></span>
```
PS C:\>Get-AzureStorageTable -Prefix "table"
```

<span data-ttu-id="d9732-115">Bu komut, adı tabloyla başlayan depolama tablolarını almak için *önek* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="d9732-115">This command uses the *Prefix* parameter to get storage tables whose name starts with table.</span></span>

## <span data-ttu-id="d9732-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d9732-116">PARAMETERS</span></span>

### <span data-ttu-id="d9732-117">-Context</span><span class="sxs-lookup"><span data-stu-id="d9732-117">-Context</span></span>
<span data-ttu-id="d9732-118">Depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9732-118">Specifies the storage context.</span></span>
<span data-ttu-id="d9732-119">Bunu oluşturmak için New-AzureStorageContext cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d9732-119">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d9732-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="d9732-120">-Name</span></span>
<span data-ttu-id="d9732-121">Tablo adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9732-121">Specifies the table name.</span></span>
<span data-ttu-id="d9732-122">Tablo adı boşsa, cmdlet tüm tabloları listeler.</span><span class="sxs-lookup"><span data-stu-id="d9732-122">If the table name is empty, the cmdlet lists all the tables.</span></span>
<span data-ttu-id="d9732-123">Aksi takdirde, belirtilen ad veya normal Ad düzeniyle eşleşen tüm tablolar listelenir.</span><span class="sxs-lookup"><span data-stu-id="d9732-123">Otherwise, it lists all tables that match the specified name or the regular name pattern.</span></span>

```yaml
Type: String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9732-124">-Önek</span><span class="sxs-lookup"><span data-stu-id="d9732-124">-Prefix</span></span>
<span data-ttu-id="d9732-125">Almak istediğiniz tablo veya tabloların adında kullanılan bir önek belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9732-125">Specifies a prefix used in the name of the table or tables you want to get.</span></span>
<span data-ttu-id="d9732-126">Tablo gibi aynı dizeyle başlayan tüm tabloları bulmak için bunu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d9732-126">You can use this to find all tables that start with the same string, such as table.</span></span>

```yaml
Type: String
Parameter Sets: TablePrefix
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9732-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9732-127">CommonParameters</span></span>
<span data-ttu-id="d9732-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d9732-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9732-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9732-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9732-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d9732-130">INPUTS</span></span>

## <span data-ttu-id="d9732-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d9732-131">OUTPUTS</span></span>

## <span data-ttu-id="d9732-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d9732-132">NOTES</span></span>

## <span data-ttu-id="d9732-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d9732-133">RELATED LINKS</span></span>

[<span data-ttu-id="d9732-134">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="d9732-134">New-AzureStorageTable</span></span>](./New-AzureStorageTable.md)

[<span data-ttu-id="d9732-135">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="d9732-135">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)


