---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTable.md
ms.openlocfilehash: 1b01550e8501a0a7f81ac5c04cd0083fc521fec5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758594"
---
# <span data-ttu-id="c2b10-101">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="c2b10-101">New-AzStorageTable</span></span>

## <span data-ttu-id="c2b10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2b10-102">SYNOPSIS</span></span>
<span data-ttu-id="c2b10-103">Depolama tablosu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c2b10-103">Creates a storage table.</span></span>

## <span data-ttu-id="c2b10-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c2b10-104">SYNTAX</span></span>

```
New-AzStorageTable [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2b10-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c2b10-105">DESCRIPTION</span></span>
<span data-ttu-id="c2b10-106">**New-AzStorageTable** cmdlet 'i Azure 'daki depolama hesabıyla ilişkilendirilmiş bir depolama tablosu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c2b10-106">The **New-AzStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="c2b10-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c2b10-107">EXAMPLES</span></span>

### <span data-ttu-id="c2b10-108">Örnek 1: Azure depolama tablosu oluşturma</span><span class="sxs-lookup"><span data-stu-id="c2b10-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzStorageTable -Name "tableabc"
```

<span data-ttu-id="c2b10-109">Bu komut, tableabc adında bir depolama tablosu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c2b10-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="c2b10-110">Örnek 2: birden çok Azure depolama tablosu oluşturma</span><span class="sxs-lookup"><span data-stu-id="c2b10-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzStorageTable
```

<span data-ttu-id="c2b10-111">Bu komut birden çok tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c2b10-111">This command creates multiple tables.</span></span>
<span data-ttu-id="c2b10-112">.NET **String** sınıfının **bölme** yöntemini kullanır ve sonra da ardışık düzene geçirir.</span><span class="sxs-lookup"><span data-stu-id="c2b10-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="c2b10-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c2b10-113">PARAMETERS</span></span>

### <span data-ttu-id="c2b10-114">-Context</span><span class="sxs-lookup"><span data-stu-id="c2b10-114">-Context</span></span>
<span data-ttu-id="c2b10-115">Depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c2b10-115">Specifies the storage context.</span></span>
<span data-ttu-id="c2b10-116">Bunu oluşturmak için New-AzStorageContext cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c2b10-116">To create it, you can use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c2b10-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2b10-117">-DefaultProfile</span></span>
<span data-ttu-id="c2b10-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c2b10-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2b10-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="c2b10-119">-Name</span></span>
<span data-ttu-id="c2b10-120">Yeni tablo için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="c2b10-120">Specifies a name for the new table.</span></span>

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

### <span data-ttu-id="c2b10-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2b10-121">CommonParameters</span></span>
<span data-ttu-id="c2b10-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c2b10-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2b10-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2b10-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2b10-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c2b10-124">INPUTS</span></span>

### <span data-ttu-id="c2b10-125">System. String</span><span class="sxs-lookup"><span data-stu-id="c2b10-125">System.String</span></span>

### <span data-ttu-id="c2b10-126">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="c2b10-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c2b10-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c2b10-127">OUTPUTS</span></span>

### <span data-ttu-id="c2b10-128">Microsoft. Windowsazde. Commands. Common. Storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="c2b10-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="c2b10-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c2b10-129">NOTES</span></span>

## <span data-ttu-id="c2b10-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c2b10-130">RELATED LINKS</span></span>

[<span data-ttu-id="c2b10-131">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="c2b10-131">Get-AzStorageTable</span></span>](./Get-AzStorageTable.md)

[<span data-ttu-id="c2b10-132">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="c2b10-132">Remove-AzStorageTable</span></span>](./Remove-AzStorageTable.md)


