---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0937A390-6AC2-4611-AA6C-99936AC0ABFD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/test-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: e9410c8bd63a123f275f6e644971870b998deea0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593258"
---
# <span data-ttu-id="18644-101">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="18644-101">Test-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="18644-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18644-102">SYNOPSIS</span></span>
<span data-ttu-id="18644-103">Data Lake Store 'da bir dosya veya klasörün varlığını sınar.</span><span class="sxs-lookup"><span data-stu-id="18644-103">Tests the existence of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18644-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="18644-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-PathType] <PathType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18644-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="18644-105">DESCRIPTION</span></span>
<span data-ttu-id="18644-106">**Test-AzureRmDataLakeStoreItem** cmdlet 'ı Data Lake Store 'da bir dosya veya klasörün varlığını sınar.</span><span class="sxs-lookup"><span data-stu-id="18644-106">The **Test-AzureRmDataLakeStoreItem** cmdlet tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="18644-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="18644-107">EXAMPLES</span></span>

### <span data-ttu-id="18644-108">Örnek 1: dosyayı test etme</span><span class="sxs-lookup"><span data-stu-id="18644-108">Example 1: Test a file</span></span>
```
PS C:\>Test-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="18644-109">Bu komut, Test.csv dosyasının ContosoADL hesabında bulunup bulunmadığını sınar.</span><span class="sxs-lookup"><span data-stu-id="18644-109">This command tests whether the file Test.csv exists in the ContosoADL account.</span></span>

## <span data-ttu-id="18644-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="18644-110">PARAMETERS</span></span>

### <span data-ttu-id="18644-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="18644-111">-Account</span></span>
<span data-ttu-id="18644-112">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="18644-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="18644-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18644-113">-DefaultProfile</span></span>
<span data-ttu-id="18644-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="18644-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18644-115">-Yol</span><span class="sxs-lookup"><span data-stu-id="18644-115">-Path</span></span>
<span data-ttu-id="18644-116">Kök dizinle (/) başlayarak sınanacak olan öğenin veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="18644-116">Specifies the Data Lake Store path of the item to test, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="18644-117">-PathType</span><span class="sxs-lookup"><span data-stu-id="18644-117">-PathType</span></span>
<span data-ttu-id="18644-118">Sınanacak öğenin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="18644-118">Specifies the type of item to test.</span></span>
<span data-ttu-id="18644-119">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="18644-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="18644-120">Tüm</span><span class="sxs-lookup"><span data-stu-id="18644-120">Any</span></span> 
- <span data-ttu-id="18644-121">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="18644-121">File</span></span> 
- <span data-ttu-id="18644-122">Klasörler</span><span class="sxs-lookup"><span data-stu-id="18644-122">Folder</span></span>

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

### <span data-ttu-id="18644-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18644-123">CommonParameters</span></span>
<span data-ttu-id="18644-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="18644-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18644-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18644-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18644-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="18644-126">INPUTS</span></span>

### <span data-ttu-id="18644-127">System. String</span><span class="sxs-lookup"><span data-stu-id="18644-127">System.String</span></span>

### <span data-ttu-id="18644-128">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="18644-128">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="18644-129">Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreEnums + PathType</span><span class="sxs-lookup"><span data-stu-id="18644-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathType</span></span>

## <span data-ttu-id="18644-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="18644-130">OUTPUTS</span></span>

### <span data-ttu-id="18644-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="18644-131">System.Boolean</span></span>

## <span data-ttu-id="18644-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="18644-132">NOTES</span></span>

## <span data-ttu-id="18644-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="18644-133">RELATED LINKS</span></span>

[<span data-ttu-id="18644-134">Dışarı aktarma-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="18644-134">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="18644-135">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="18644-135">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="18644-136">İçeri aktarma-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="18644-136">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="18644-137">Katıl-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="18644-137">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="18644-138">Taşı-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="18644-138">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="18644-139">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="18644-139">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)


