---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-azstorageblobqueryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobQueryConfig.md
ms.openlocfilehash: ec1b3b7ab7cd0ddbbdb0b938149f03755563a742
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273798"
---
# <span data-ttu-id="19170-101">New-AzStorageBlobQueryConfig</span><span class="sxs-lookup"><span data-stu-id="19170-101">New-AzStorageBlobQueryConfig</span></span>

## <span data-ttu-id="19170-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19170-102">SYNOPSIS</span></span>
<span data-ttu-id="19170-103">Get-AzStorageBlobQueryResult 'da kullanılabilen bir blob sorgu yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="19170-103">Creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="19170-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="19170-104">SYNTAX</span></span>

### <span data-ttu-id="19170-105">CSV (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="19170-105">Csv (Default)</span></span>
```
New-AzStorageBlobQueryConfig [-AsCsv] [-RecordSeparator <String>] [-ColumnSeparator <String>]
 [-QuotationCharacter <Char>] [-EscapeCharacter <Char>] [-HasHeader] [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="19170-106">JSON</span><span class="sxs-lookup"><span data-stu-id="19170-106">Json</span></span>
```
New-AzStorageBlobQueryConfig [-AsJson] [-RecordSeparator <String>] [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="19170-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="19170-107">DESCRIPTION</span></span>
<span data-ttu-id="19170-108">**New-AzStorageBlobQueryConfig** cmdlet 'i Get-AzStorageBlobQueryResult 'da kullanılabilen bir blob sorgu yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="19170-108">The **New-AzStorageBlobQueryConfig** cmdlet creates a blob query configuration object, which can be used in Get-AzStorageBlobQueryResult.</span></span>

## <span data-ttu-id="19170-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="19170-109">EXAMPLES</span></span>

### <span data-ttu-id="19170-110">Örnek 1: blob sorgusu oluşturma</span><span class="sxs-lookup"><span data-stu-id="19170-110">Example 1: Create blob query configures , and query a blob</span></span>
```powershell
PS C:\> $inputconfig = New-AzStorageBlobQueryConfig -AsCsv -ColumnSeparator "," -QuotationCharacter """" -EscapeCharacter "\" -RecordSeparator "`n" -HasHeader

PS C:\> $outputconfig = New-AzStorageBlobQueryConfig -AsJson -RecordSeparator "`n" 

PS C:\> $queryString = "SELECT * FROM BlobStorage WHERE Name = 'a'"

PS C:\> $result = Get-AzStorageBlobQueryResult -Container $containerName -Blob $blobName -QueryString $queryString -ResultFile "c:\resultfile.json" -InputTextConfiguration $inputconfig -OutputTextConfiguration $outputconfig -Context $ctx

PS C:\> $result

BytesScanned FailureCount BlobQueryError
------------ ------------ --------------
         449            0
```

<span data-ttu-id="19170-111">Bu komut öncelikle giriş yapılandırma nesnesini CSV olarak ve çıktı yapılandırma nesnesini JSON olarak oluşturun, sonra da 2 yapılandırmayı kullanarak blob 'u sorgulayın.</span><span class="sxs-lookup"><span data-stu-id="19170-111">This command first create input configuration object as csv, and output configuration object as json, then use the 2 configurations to query blob.</span></span>

## <span data-ttu-id="19170-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="19170-112">PARAMETERS</span></span>

### <span data-ttu-id="19170-113">-Yoksv</span><span class="sxs-lookup"><span data-stu-id="19170-113">-AsCsv</span></span>
<span data-ttu-id="19170-114">CSV için blob sorgu yapılandırması oluşturulacağını belirtin.</span><span class="sxs-lookup"><span data-stu-id="19170-114">Indicate to create a Blob Query Configuration for CSV.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Csv
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19170-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="19170-115">-AsJob</span></span>
<span data-ttu-id="19170-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="19170-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19170-117">-AsJson</span><span class="sxs-lookup"><span data-stu-id="19170-117">-AsJson</span></span>
<span data-ttu-id="19170-118">JSON için blob sorgu yapılandırması oluşturulacağını belirtin.</span><span class="sxs-lookup"><span data-stu-id="19170-118">Indicate to create a Blob Query Configuration for Json.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Json
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19170-119">-ColumnSeparator</span><span class="sxs-lookup"><span data-stu-id="19170-119">-ColumnSeparator</span></span>
<span data-ttu-id="19170-120">İsteğe.</span><span class="sxs-lookup"><span data-stu-id="19170-120">Optional.</span></span>
<span data-ttu-id="19170-121">Sütunları ayırmak için kullanılan dize.</span><span class="sxs-lookup"><span data-stu-id="19170-121">The string used to separate columns.</span></span>

```yaml
Type: System.String
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19170-122">-EscapeCharacter</span><span class="sxs-lookup"><span data-stu-id="19170-122">-EscapeCharacter</span></span>
<span data-ttu-id="19170-123">İsteğe.</span><span class="sxs-lookup"><span data-stu-id="19170-123">Optional.</span></span>
<span data-ttu-id="19170-124">Kaçış karakteri olarak kullanılan karakter.</span><span class="sxs-lookup"><span data-stu-id="19170-124">The char used as an escape character.</span></span>

```yaml
Type: System.Nullable`1[System.Char]
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19170-125">-HasHeader</span><span class="sxs-lookup"><span data-stu-id="19170-125">-HasHeader</span></span>
<span data-ttu-id="19170-126">İsteğe.</span><span class="sxs-lookup"><span data-stu-id="19170-126">Optional.</span></span>
<span data-ttu-id="19170-127">Verilerin üst bilgi olduğunu temsil ettiğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="19170-127">Indicate it represent the data has headers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19170-128">-QuotationCharacter</span><span class="sxs-lookup"><span data-stu-id="19170-128">-QuotationCharacter</span></span>
<span data-ttu-id="19170-129">İsteğe.</span><span class="sxs-lookup"><span data-stu-id="19170-129">Optional.</span></span>
<span data-ttu-id="19170-130">Belirli bir alanı tırnak içine almak için kullanılan karakter.</span><span class="sxs-lookup"><span data-stu-id="19170-130">The char used to quote a specific field.</span></span>

```yaml
Type: System.Char
Parameter Sets: Csv
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19170-131">-RecordSeparator</span><span class="sxs-lookup"><span data-stu-id="19170-131">-RecordSeparator</span></span>
<span data-ttu-id="19170-132">İsteğe.</span><span class="sxs-lookup"><span data-stu-id="19170-132">Optional.</span></span>
<span data-ttu-id="19170-133">Kayıtları ayırmak için kullanılan dize.</span><span class="sxs-lookup"><span data-stu-id="19170-133">The string used to separate records.</span></span>

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

### <span data-ttu-id="19170-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19170-134">CommonParameters</span></span>
<span data-ttu-id="19170-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="19170-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19170-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19170-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19170-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="19170-137">INPUTS</span></span>

### <span data-ttu-id="19170-138">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="19170-138">None</span></span>

## <span data-ttu-id="19170-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="19170-139">OUTPUTS</span></span>

### <span data-ttu-id="19170-140">Microsoft. Windowsazde. Commands. Common. Storage. ResourceModel. PSBlobQueryTextConfiguration</span><span class="sxs-lookup"><span data-stu-id="19170-140">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.PSBlobQueryTextConfiguration</span></span>

## <span data-ttu-id="19170-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="19170-141">NOTES</span></span>

## <span data-ttu-id="19170-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="19170-142">RELATED LINKS</span></span>
