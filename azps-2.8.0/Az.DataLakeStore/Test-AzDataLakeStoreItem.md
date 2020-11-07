---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0937A390-6AC2-4611-AA6C-99936AC0ABFD
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/test-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreItem.md
ms.openlocfilehash: c79e8c225fbbc901d9c39eed85d795cf27d6d1d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752265"
---
# <span data-ttu-id="9fe3c-101">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9fe3c-101">Test-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="9fe3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fe3c-102">SYNOPSIS</span></span>
<span data-ttu-id="9fe3c-103">Data Lake Store 'da bir dosya veya klasörün varlığını sınar.</span><span class="sxs-lookup"><span data-stu-id="9fe3c-103">Tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="9fe3c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9fe3c-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-PathType] <PathType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9fe3c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9fe3c-105">DESCRIPTION</span></span>
<span data-ttu-id="9fe3c-106">**Test-AzDataLakeStoreItem** cmdlet 'ı Data Lake Store 'da bir dosya veya klasörün varlığını sınar.</span><span class="sxs-lookup"><span data-stu-id="9fe3c-106">The **Test-AzDataLakeStoreItem** cmdlet tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="9fe3c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9fe3c-107">EXAMPLES</span></span>

### <span data-ttu-id="9fe3c-108">Örnek 1: dosyayı test etme</span><span class="sxs-lookup"><span data-stu-id="9fe3c-108">Example 1: Test a file</span></span>
```
PS C:\>Test-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="9fe3c-109">Bu komut, Test.csv dosyasının ContosoADL hesabında bulunup bulunmadığını sınar.</span><span class="sxs-lookup"><span data-stu-id="9fe3c-109">This command tests whether the file Test.csv exists in the ContosoADL account.</span></span>

## <span data-ttu-id="9fe3c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9fe3c-110">PARAMETERS</span></span>

### <span data-ttu-id="9fe3c-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="9fe3c-111">-Account</span></span>
<span data-ttu-id="9fe3c-112">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9fe3c-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe3c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fe3c-113">-DefaultProfile</span></span>
<span data-ttu-id="9fe3c-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9fe3c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fe3c-115">-Yol</span><span class="sxs-lookup"><span data-stu-id="9fe3c-115">-Path</span></span>
<span data-ttu-id="9fe3c-116">Kök dizinle (/) başlayarak sınanacak olan öğenin veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="9fe3c-116">Specifies the Data Lake Store path of the item to test, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe3c-117">-PathType</span><span class="sxs-lookup"><span data-stu-id="9fe3c-117">-PathType</span></span>
<span data-ttu-id="9fe3c-118">Sınanacak öğenin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="9fe3c-118">Specifies the type of item to test.</span></span>
<span data-ttu-id="9fe3c-119">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="9fe3c-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9fe3c-120">Tüm</span><span class="sxs-lookup"><span data-stu-id="9fe3c-120">Any</span></span> 
- <span data-ttu-id="9fe3c-121">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="9fe3c-121">File</span></span> 
- <span data-ttu-id="9fe3c-122">Klasörler</span><span class="sxs-lookup"><span data-stu-id="9fe3c-122">Folder</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathType
Parameter Sets: (All)
Aliases:
Accepted values: Any, File, Folder

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fe3c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fe3c-123">CommonParameters</span></span>
<span data-ttu-id="9fe3c-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9fe3c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fe3c-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fe3c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fe3c-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9fe3c-126">INPUTS</span></span>

### <span data-ttu-id="9fe3c-127">System. String</span><span class="sxs-lookup"><span data-stu-id="9fe3c-127">System.String</span></span>

### <span data-ttu-id="9fe3c-128">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="9fe3c-128">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="9fe3c-129">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreEnums + PathType</span><span class="sxs-lookup"><span data-stu-id="9fe3c-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathType</span></span>

## <span data-ttu-id="9fe3c-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9fe3c-130">OUTPUTS</span></span>

### <span data-ttu-id="9fe3c-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9fe3c-131">System.Boolean</span></span>

## <span data-ttu-id="9fe3c-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9fe3c-132">NOTES</span></span>

## <span data-ttu-id="9fe3c-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9fe3c-133">RELATED LINKS</span></span>

[<span data-ttu-id="9fe3c-134">Dışarı aktarma-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9fe3c-134">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="9fe3c-135">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9fe3c-135">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="9fe3c-136">İçeri aktarma-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9fe3c-136">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="9fe3c-137">Katıl-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9fe3c-137">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="9fe3c-138">Taşı-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9fe3c-138">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="9fe3c-139">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9fe3c-139">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

