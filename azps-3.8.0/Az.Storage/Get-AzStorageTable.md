---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
ms.openlocfilehash: d501faaebcc5e381dc2a7270c8b55b148e2812b4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097756"
---
# <span data-ttu-id="7aad9-101">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="7aad9-101">Get-AzStorageTable</span></span>

## <span data-ttu-id="7aad9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7aad9-102">SYNOPSIS</span></span>
<span data-ttu-id="7aad9-103">Depolama tablolarını listeler.</span><span class="sxs-lookup"><span data-stu-id="7aad9-103">Lists the storage tables.</span></span>

## <span data-ttu-id="7aad9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7aad9-104">SYNTAX</span></span>

### <span data-ttu-id="7aad9-105">TableName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7aad9-105">TableName (Default)</span></span>
```
Get-AzStorageTable [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7aad9-106">TablePrefix</span><span class="sxs-lookup"><span data-stu-id="7aad9-106">TablePrefix</span></span>
```
Get-AzStorageTable -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7aad9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7aad9-107">DESCRIPTION</span></span>
<span data-ttu-id="7aad9-108">**Get-AzStorageTable** cmdlet 'ı, Azure 'daki depolama hesabıyla ilişkilendirilmiş depolama tablolarını listeler.</span><span class="sxs-lookup"><span data-stu-id="7aad9-108">The **Get-AzStorageTable** cmdlet lists the storage tables associated with the storage account in Azure.</span></span>

## <span data-ttu-id="7aad9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7aad9-109">EXAMPLES</span></span>

### <span data-ttu-id="7aad9-110">Örnek 1: tüm Azure depolama tablolarını listeler</span><span class="sxs-lookup"><span data-stu-id="7aad9-110">Example 1: List all Azure Storage tables</span></span>
```
PS C:\>Get-AzStorageTable
```

<span data-ttu-id="7aad9-111">Bu komut, depolama hesabının tüm depolama tablolarını alır.</span><span class="sxs-lookup"><span data-stu-id="7aad9-111">This command gets all storage tables for a Storage account.</span></span>

### <span data-ttu-id="7aad9-112">Örnek 2: joker karakter kullanarak Azure depolama tablolarını listeleme</span><span class="sxs-lookup"><span data-stu-id="7aad9-112">Example 2: List Azure Storage tables using a wildcard character</span></span>
```
PS C:\>Get-AzStorageTable -Name table*
```

<span data-ttu-id="7aad9-113">Bu komut, adı tabloyla başlayan depolama tablolarını almak için joker karakter kullanır.</span><span class="sxs-lookup"><span data-stu-id="7aad9-113">This command uses a wildcard character to get storage tables whose name starts with table.</span></span>

### <span data-ttu-id="7aad9-114">Örnek 3: tablo adı önekini kullanarak Azure depolama tablolarını listeleme</span><span class="sxs-lookup"><span data-stu-id="7aad9-114">Example 3: List Azure Storage tables using table name prefix</span></span>
```
PS C:\>Get-AzStorageTable -Prefix "table"
```

<span data-ttu-id="7aad9-115">Bu komut, adı tabloyla başlayan depolama tablolarını almak için *önek* parametresini kullanır.</span><span class="sxs-lookup"><span data-stu-id="7aad9-115">This command uses the *Prefix* parameter to get storage tables whose name starts with table.</span></span>

## <span data-ttu-id="7aad9-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7aad9-116">PARAMETERS</span></span>

### <span data-ttu-id="7aad9-117">-Context</span><span class="sxs-lookup"><span data-stu-id="7aad9-117">-Context</span></span>
<span data-ttu-id="7aad9-118">Depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7aad9-118">Specifies the storage context.</span></span>
<span data-ttu-id="7aad9-119">Bunu oluşturmak için New-AzStorageContext cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7aad9-119">To create it, you can use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7aad9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7aad9-120">-DefaultProfile</span></span>
<span data-ttu-id="7aad9-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7aad9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7aad9-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="7aad9-122">-Name</span></span>
<span data-ttu-id="7aad9-123">Tablo adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7aad9-123">Specifies the table name.</span></span>
<span data-ttu-id="7aad9-124">Tablo adı boşsa, cmdlet tüm tabloları listeler.</span><span class="sxs-lookup"><span data-stu-id="7aad9-124">If the table name is empty, the cmdlet lists all the tables.</span></span>
<span data-ttu-id="7aad9-125">Aksi takdirde, belirtilen ad veya normal Ad düzeniyle eşleşen tüm tablolar listelenir.</span><span class="sxs-lookup"><span data-stu-id="7aad9-125">Otherwise, it lists all tables that match the specified name or the regular name pattern.</span></span>

```yaml
Type: System.String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7aad9-126">-Önek</span><span class="sxs-lookup"><span data-stu-id="7aad9-126">-Prefix</span></span>
<span data-ttu-id="7aad9-127">Almak istediğiniz tablo veya tabloların adında kullanılan bir önek belirtir.</span><span class="sxs-lookup"><span data-stu-id="7aad9-127">Specifies a prefix used in the name of the table or tables you want to get.</span></span>
<span data-ttu-id="7aad9-128">Tablo gibi aynı dizeyle başlayan tüm tabloları bulmak için bunu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7aad9-128">You can use this to find all tables that start with the same string, such as table.</span></span>

```yaml
Type: System.String
Parameter Sets: TablePrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7aad9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7aad9-129">CommonParameters</span></span>
<span data-ttu-id="7aad9-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7aad9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7aad9-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7aad9-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7aad9-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7aad9-132">INPUTS</span></span>

### <span data-ttu-id="7aad9-133">System. String</span><span class="sxs-lookup"><span data-stu-id="7aad9-133">System.String</span></span>

### <span data-ttu-id="7aad9-134">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="7aad9-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7aad9-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7aad9-135">OUTPUTS</span></span>

### <span data-ttu-id="7aad9-136">Microsoft. Windowsazde. Commands. Common. Storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="7aad9-136">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="7aad9-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7aad9-137">NOTES</span></span>

## <span data-ttu-id="7aad9-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7aad9-138">RELATED LINKS</span></span>

[<span data-ttu-id="7aad9-139">Yeni-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="7aad9-139">New-AzStorageTable</span></span>](./New-AzStorageTable.md)

[<span data-ttu-id="7aad9-140">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="7aad9-140">Remove-AzStorageTable</span></span>](./Remove-AzStorageTable.md)


