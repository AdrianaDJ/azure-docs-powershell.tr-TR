---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 00CCA9B8-7C57-4FC0-9BD1-5FC16010E820
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/move-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Move-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Move-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 5e6fb437833db3f4278335f67693d084c2d6d95b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762650"
---
# <span data-ttu-id="95695-101">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="95695-101">Move-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="95695-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95695-102">SYNOPSIS</span></span>
<span data-ttu-id="95695-103">Data Lake Store 'da bir dosyayı veya klasörü taşıma veya yeniden adlandırmıştır.</span><span class="sxs-lookup"><span data-stu-id="95695-103">Moves or renames a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95695-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="95695-104">SYNTAX</span></span>

```
Move-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95695-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="95695-105">DESCRIPTION</span></span>
<span data-ttu-id="95695-106">**Taþý-AzureRmDataLakeStoreItem** cmdlet 'ı Data Lake Store 'da bir dosyayı veya klasörü taşır veya yeniden adlandırır.</span><span class="sxs-lookup"><span data-stu-id="95695-106">The **Move-AzureRmDataLakeStoreItem** cmdlet moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="95695-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="95695-107">EXAMPLES</span></span>

### <span data-ttu-id="95695-108">Örnek 1: öğeyi taşıma ve yeniden adlandırma</span><span class="sxs-lookup"><span data-stu-id="95695-108">Example 1: Move and rename an item</span></span>
```
PS C:\>Move-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/Original/Path/File.txt" -Destination "/New/Path/RenamedFile.txt"
```

<span data-ttu-id="95695-109">Bu komut RenamedFile.txt için öğe File.txt yeniden adlandırır ve farklı bir klasöre taşımıştır.</span><span class="sxs-lookup"><span data-stu-id="95695-109">This command renames the item File.txt to RenamedFile.txt and moves it to a different folder.</span></span>

## <span data-ttu-id="95695-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="95695-110">PARAMETERS</span></span>

### <span data-ttu-id="95695-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="95695-111">-Account</span></span>
<span data-ttu-id="95695-112">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="95695-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95695-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95695-113">-DefaultProfile</span></span>
<span data-ttu-id="95695-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="95695-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95695-115">-Hedef</span><span class="sxs-lookup"><span data-stu-id="95695-115">-Destination</span></span>
<span data-ttu-id="95695-116">Kök dizinden (/) başlayarak öğenin taşınacağı Data Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="95695-116">Specifies the Data Lake Store path to which to move the item, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95695-117">-Force</span><span class="sxs-lookup"><span data-stu-id="95695-117">-Force</span></span>
<span data-ttu-id="95695-118">Zaten varsa, bu işlemin hedef dosyanın üzerine yazabileceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="95695-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95695-119">-Yol</span><span class="sxs-lookup"><span data-stu-id="95695-119">-Path</span></span>
<span data-ttu-id="95695-120">Kök dizinden (/) başlayarak taşınacak veya yeniden adlandırılacak öğenin veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="95695-120">Specifies the Data Lake Store path of the item to move or rename, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95695-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="95695-121">-Confirm</span></span>
<span data-ttu-id="95695-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="95695-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95695-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95695-123">-WhatIf</span></span>
<span data-ttu-id="95695-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="95695-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95695-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="95695-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95695-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95695-126">CommonParameters</span></span>
<span data-ttu-id="95695-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="95695-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95695-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95695-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95695-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="95695-129">INPUTS</span></span>

### <span data-ttu-id="95695-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="95695-130">None</span></span>
<span data-ttu-id="95695-131">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="95695-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="95695-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="95695-132">OUTPUTS</span></span>

### <span data-ttu-id="95695-133">dizisi</span><span class="sxs-lookup"><span data-stu-id="95695-133">string</span></span>
<span data-ttu-id="95695-134">Taşınan dosyanın veya klasörün tam yolu.</span><span class="sxs-lookup"><span data-stu-id="95695-134">The full path to the moved file or folder.</span></span>

## <span data-ttu-id="95695-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="95695-135">NOTES</span></span>

## <span data-ttu-id="95695-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="95695-136">RELATED LINKS</span></span>

[<span data-ttu-id="95695-137">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="95695-137">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="95695-138">Dışarı aktarma-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="95695-138">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="95695-139">İçeri aktarma-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="95695-139">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="95695-140">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="95695-140">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="95695-141">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="95695-141">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="95695-142">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="95695-142">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)

