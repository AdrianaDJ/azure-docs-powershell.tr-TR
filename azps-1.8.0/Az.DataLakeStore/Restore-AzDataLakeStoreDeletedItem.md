---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D231E9A0-DC1E-411B-A87A-56A8C767F6C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/restore-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: d674376325c103f6e3e8e0368f0db6c64422c97b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761054"
---
# <span data-ttu-id="68e90-101">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="68e90-101">Restore-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="68e90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68e90-102">SYNOPSIS</span></span>
<span data-ttu-id="68e90-103">Azure Data Lake 'ta silinmiş bir dosyayı veya klasörü geri yükleyin.</span><span class="sxs-lookup"><span data-stu-id="68e90-103">Restore a deleted file or folder in Azure Data Lake.</span></span>

## <span data-ttu-id="68e90-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="68e90-104">SYNTAX</span></span>

### <span data-ttu-id="68e90-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="68e90-105">Default (Default)</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-Path] <String> [-Destination] <String>
 [-Type] <String> [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="68e90-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="68e90-106">InputObject</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-DeletedItem] <DataLakeStoreDeletedItem>
 [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="68e90-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="68e90-107">DESCRIPTION</span></span>
<span data-ttu-id="68e90-108">**Restore-AzDataLakeStoreDeletedItem** cmdlet 'ı Data Lake Store 'da silinmiş bir dosyayı veya klasörü geri yükler.</span><span class="sxs-lookup"><span data-stu-id="68e90-108">The **Restore-AzDataLakeStoreDeletedItem** cmdlet restores a deleted file or folder in Data Lake Store.</span></span> <span data-ttu-id="68e90-109">Get-AzDataLakeStoreDeletedItem tarafından çöp retunred 'de silinmiş öğenin yolunu gerektirir.</span><span class="sxs-lookup"><span data-stu-id="68e90-109">Requires the path of deleted item in trash retunred by Get-AzDataLakeStoreDeletedItem.</span></span>

## <span data-ttu-id="68e90-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="68e90-110">EXAMPLES</span></span>

### <span data-ttu-id="68e90-111">Örnek 1:-Force seçeneğini kullanarak veri Lake Store 'dan bir dosyayı geri yükleme</span><span class="sxs-lookup"><span data-stu-id="68e90-111">Example 1: Restore a file from the Data Lake Store using -force option</span></span>
```
PS > Restore-AzDataLakeStoreDeletedItem -Account ml1ptrashtest -Path 927e8fb1-a287-4353-b50e-3b4a39ae4088 -Destination adl://ml1ptrashtest.azuredatalake.com/test0/file_1230 -Type "file" -Force
PS >

### Example 2: Restore a file from Data Lake Store using user confirmation

PS > restore-azdatalakestoredeleteditem -account ml1ptrashtest -path 927e8fb1-a287-4353-b50e-3b4a39ae4088 -destination adl://ml1ptrashtest.azuredatalake.com/test4/file_1115 -type file

Restore user data ?
From - 927e8fb1-a287-4353-b50e-3b4a39ae4088
To   - adl://ml1ptrashtest.azuredatalake.com/test4/file_1115
Type - file
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
PS >
```

## <span data-ttu-id="68e90-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="68e90-112">PARAMETERS</span></span>

### <span data-ttu-id="68e90-113">-Hesap</span><span class="sxs-lookup"><span data-stu-id="68e90-113">-Account</span></span>
<span data-ttu-id="68e90-114">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="68e90-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="68e90-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68e90-115">-DefaultProfile</span></span>
<span data-ttu-id="68e90-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="68e90-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68e90-117">-Deletedıtem</span><span class="sxs-lookup"><span data-stu-id="68e90-117">-DeletedItem</span></span>
<span data-ttu-id="68e90-118">Silinmiş öğe nesnesi.</span><span class="sxs-lookup"><span data-stu-id="68e90-118">The deleted item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68e90-119">-Hedef</span><span class="sxs-lookup"><span data-stu-id="68e90-119">-Destination</span></span>
<span data-ttu-id="68e90-120">Silinen dosyanın veya klasörün geri yüklenmesi gereken hedef yol.</span><span class="sxs-lookup"><span data-stu-id="68e90-120">The destination path to where the deleted file or folder should be restored.</span></span> 

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68e90-121">-Force</span><span class="sxs-lookup"><span data-stu-id="68e90-121">-Force</span></span>
<span data-ttu-id="68e90-122">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="68e90-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="68e90-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="68e90-123">-PassThru</span></span>
<span data-ttu-id="68e90-124">Başarı durumunda Boole değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="68e90-124">Return boolean true on success.</span></span>

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

### <span data-ttu-id="68e90-125">-Yol</span><span class="sxs-lookup"><span data-stu-id="68e90-125">-Path</span></span>
<span data-ttu-id="68e90-126">Çöp kutusundaki silinmiş dosyanın veya klasörün yolu.</span><span class="sxs-lookup"><span data-stu-id="68e90-126">The path of the deleted file or folder in trash.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68e90-127">-RestoreAction</span><span class="sxs-lookup"><span data-stu-id="68e90-127">-RestoreAction</span></span>
<span data-ttu-id="68e90-128">Hedef adı çakışmalarıyla ilgili eylem</span><span class="sxs-lookup"><span data-stu-id="68e90-128">Action to take on destination name conflicts - "copy" or "overwrite"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68e90-129">-Tür</span><span class="sxs-lookup"><span data-stu-id="68e90-129">-Type</span></span>
<span data-ttu-id="68e90-130">Geri yüklenen girdinin türü-"dosya" veya "klasör"</span><span class="sxs-lookup"><span data-stu-id="68e90-130">The type of entry being restored - "file" or "folder"</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68e90-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68e90-131">CommonParameters</span></span>
<span data-ttu-id="68e90-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="68e90-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68e90-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68e90-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68e90-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="68e90-134">INPUTS</span></span>

### <span data-ttu-id="68e90-135">System. String</span><span class="sxs-lookup"><span data-stu-id="68e90-135">System.String</span></span>

## <span data-ttu-id="68e90-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="68e90-136">OUTPUTS</span></span>

### <span data-ttu-id="68e90-137">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="68e90-137">None</span></span>

## <span data-ttu-id="68e90-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="68e90-138">NOTES</span></span>

## <span data-ttu-id="68e90-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="68e90-139">RELATED LINKS</span></span>

[<span data-ttu-id="68e90-140">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="68e90-140">Get-AzDataLakeStoreDeletedItem</span></span>](./Get-AzDataLakeStoreDeletedItem.md)