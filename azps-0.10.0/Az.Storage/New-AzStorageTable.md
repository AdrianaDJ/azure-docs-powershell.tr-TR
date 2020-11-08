---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageTable.md
ms.openlocfilehash: 29b2bb0c6a9c6e8e34c08a7ce04ca1c3ed071c84
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936209"
---
# <span data-ttu-id="27600-101">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="27600-101">New-AzStorageTable</span></span>

## <span data-ttu-id="27600-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27600-102">SYNOPSIS</span></span>
<span data-ttu-id="27600-103">Depolama tablosu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="27600-103">Creates a storage table.</span></span>

## <span data-ttu-id="27600-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="27600-104">SYNTAX</span></span>

```
New-AzStorageTable [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="27600-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="27600-105">DESCRIPTION</span></span>
<span data-ttu-id="27600-106">**New-AzStorageTable** cmdlet 'i Azure 'daki depolama hesabıyla ilişkilendirilmiş bir depolama tablosu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="27600-106">The **New-AzStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="27600-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="27600-107">EXAMPLES</span></span>

### <span data-ttu-id="27600-108">Örnek 1: Azure depolama tablosu oluşturma</span><span class="sxs-lookup"><span data-stu-id="27600-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzStorageTable -Name "tableabc"
```

<span data-ttu-id="27600-109">Bu komut, tableabc adında bir depolama tablosu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="27600-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="27600-110">Örnek 2: birden çok Azure depolama tablosu oluşturma</span><span class="sxs-lookup"><span data-stu-id="27600-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzStorageTable
```

<span data-ttu-id="27600-111">Bu komut birden çok tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="27600-111">This command creates multiple tables.</span></span>
<span data-ttu-id="27600-112">.NET **String** sınıfının **bölme** yöntemini kullanır ve sonra da ardışık düzene geçirir.</span><span class="sxs-lookup"><span data-stu-id="27600-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="27600-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="27600-113">PARAMETERS</span></span>

### <span data-ttu-id="27600-114">-Context</span><span class="sxs-lookup"><span data-stu-id="27600-114">-Context</span></span>
<span data-ttu-id="27600-115">Depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="27600-115">Specifies the storage context.</span></span>
<span data-ttu-id="27600-116">Bunu oluşturmak için New-AzStorageContext cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27600-116">To create it, you can use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="27600-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27600-117">-DefaultProfile</span></span>
<span data-ttu-id="27600-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="27600-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27600-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="27600-119">-Name</span></span>
<span data-ttu-id="27600-120">Yeni tablo için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="27600-120">Specifies a name for the new table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27600-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27600-121">CommonParameters</span></span>
<span data-ttu-id="27600-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="27600-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27600-123">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27600-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27600-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="27600-124">INPUTS</span></span>

### <span data-ttu-id="27600-125">System. String</span><span class="sxs-lookup"><span data-stu-id="27600-125">System.String</span></span>

### <span data-ttu-id="27600-126">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="27600-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="27600-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="27600-127">OUTPUTS</span></span>

### <span data-ttu-id="27600-128">Microsoft. Windowsazde. Commands. Common. Storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="27600-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="27600-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="27600-129">NOTES</span></span>

## <span data-ttu-id="27600-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="27600-130">RELATED LINKS</span></span>

[<span data-ttu-id="27600-131">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="27600-131">Get-AzStorageTable</span></span>](./Get-AzStorageTable.md)

[<span data-ttu-id="27600-132">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="27600-132">Remove-AzStorageTable</span></span>](./Remove-AzStorageTable.md)

