---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D231E9A0-DC1E-411B-A87A-56A8C767F6C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/restore-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: 9dcc45f8f082ce59a6082ad71c2084c5df10064c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320510"
---
# <span data-ttu-id="f9e70-101">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="f9e70-101">Restore-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="f9e70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9e70-102">SYNOPSIS</span></span>
<span data-ttu-id="f9e70-103">Azure Data Lake 'ta silinmiş bir dosyayı veya klasörü geri yükleyin.</span><span class="sxs-lookup"><span data-stu-id="f9e70-103">Restore a deleted file or folder in Azure Data Lake.</span></span>

## <span data-ttu-id="f9e70-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f9e70-104">SYNTAX</span></span>

### <span data-ttu-id="f9e70-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f9e70-105">Default (Default)</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-Path] <String> [-Destination] <String>
 [-Type] <String> [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f9e70-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f9e70-106">InputObject</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-DeletedItem] <DataLakeStoreDeletedItem>
 [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f9e70-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f9e70-107">DESCRIPTION</span></span>
<span data-ttu-id="f9e70-108">**Restore-AzDataLakeStoreDeletedItem** cmdlet 'ı Data Lake Store 'da silinmiş bir dosyayı veya klasörü geri yükler.</span><span class="sxs-lookup"><span data-stu-id="f9e70-108">The **Restore-AzDataLakeStoreDeletedItem** cmdlet restores a deleted file or folder in Data Lake Store.</span></span> <span data-ttu-id="f9e70-109">Çöp kutusunda Get-AzDataLakeStoreDeletedItem tarafından döndürülen silinmiş öğenin yolunu gerektirir.</span><span class="sxs-lookup"><span data-stu-id="f9e70-109">Requires the path of deleted item in trash returned by Get-AzDataLakeStoreDeletedItem.</span></span>
<span data-ttu-id="f9e70-110">Dikkat: dosyaların silinmesini kaldırma işlemi en iyi çaba işlemidir.</span><span class="sxs-lookup"><span data-stu-id="f9e70-110">Caution: Undeleting files is a best effort operation.</span></span> <span data-ttu-id="f9e70-111">Bir dosyanın silindikten sonra geri yüklenebileceğini garanti etmez.</span><span class="sxs-lookup"><span data-stu-id="f9e70-111">There are no guarantees that a file can be restored once it is deleted.</span></span> <span data-ttu-id="f9e70-112">Bu API kullanımı, Whitelist ile etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="f9e70-112">The use of this API is enabled via whitelisting.</span></span> <span data-ttu-id="f9e70-113">ADL hesabınız beyaz listelenmezse, bu API 'yi kullanmak throw özel durumuna uygulanmaz.</span><span class="sxs-lookup"><span data-stu-id="f9e70-113">If your ADL account is not whitelisted, then using this api will throw Not implemented exception.</span></span> <span data-ttu-id="f9e70-114">Daha fazla bilgi ve yardım için lütfen Microsoft desteğine başvurun.</span><span class="sxs-lookup"><span data-stu-id="f9e70-114">For further information and assistance please contact Microsoft support.</span></span>

## <span data-ttu-id="f9e70-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f9e70-115">EXAMPLES</span></span>

### <span data-ttu-id="f9e70-116">Örnek 1:-Force seçeneğini kullanarak veri Lake Store 'dan bir dosyayı geri yükleme</span><span class="sxs-lookup"><span data-stu-id="f9e70-116">Example 1: Restore a file from the Data Lake Store using -force option</span></span>
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

## <span data-ttu-id="f9e70-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f9e70-117">PARAMETERS</span></span>

### <span data-ttu-id="f9e70-118">-Hesap</span><span class="sxs-lookup"><span data-stu-id="f9e70-118">-Account</span></span>
<span data-ttu-id="f9e70-119">Data Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f9e70-119">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="f9e70-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9e70-120">-DefaultProfile</span></span>
<span data-ttu-id="f9e70-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f9e70-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9e70-122">-Deletedıtem</span><span class="sxs-lookup"><span data-stu-id="f9e70-122">-DeletedItem</span></span>
<span data-ttu-id="f9e70-123">Silinmiş öğe nesnesi.</span><span class="sxs-lookup"><span data-stu-id="f9e70-123">The deleted item object.</span></span>

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

### <span data-ttu-id="f9e70-124">-Hedef</span><span class="sxs-lookup"><span data-stu-id="f9e70-124">-Destination</span></span>
<span data-ttu-id="f9e70-125">Silinen dosyanın veya klasörün geri yüklenmesi gereken hedef yol.</span><span class="sxs-lookup"><span data-stu-id="f9e70-125">The destination path to where the deleted file or folder should be restored.</span></span> 

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

### <span data-ttu-id="f9e70-126">-Force</span><span class="sxs-lookup"><span data-stu-id="f9e70-126">-Force</span></span>
<span data-ttu-id="f9e70-127">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="f9e70-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f9e70-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f9e70-128">-PassThru</span></span>
<span data-ttu-id="f9e70-129">Başarı durumunda Boole değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="f9e70-129">Return boolean true on success.</span></span>

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

### <span data-ttu-id="f9e70-130">-Yol</span><span class="sxs-lookup"><span data-stu-id="f9e70-130">-Path</span></span>
<span data-ttu-id="f9e70-131">Çöp kutusundaki silinmiş dosyanın veya klasörün yolu.</span><span class="sxs-lookup"><span data-stu-id="f9e70-131">The path of the deleted file or folder in trash.</span></span>

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

### <span data-ttu-id="f9e70-132">-RestoreAction</span><span class="sxs-lookup"><span data-stu-id="f9e70-132">-RestoreAction</span></span>
<span data-ttu-id="f9e70-133">Hedef adı çakışmalarıyla ilgili eylem</span><span class="sxs-lookup"><span data-stu-id="f9e70-133">Action to take on destination name conflicts - "copy" or "overwrite"</span></span>

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

### <span data-ttu-id="f9e70-134">-Tür</span><span class="sxs-lookup"><span data-stu-id="f9e70-134">-Type</span></span>
<span data-ttu-id="f9e70-135">Geri yüklenen girdinin türü-"dosya" veya "klasör"</span><span class="sxs-lookup"><span data-stu-id="f9e70-135">The type of entry being restored - "file" or "folder"</span></span>

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

### <span data-ttu-id="f9e70-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9e70-136">CommonParameters</span></span>
<span data-ttu-id="f9e70-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f9e70-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9e70-138">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9e70-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9e70-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f9e70-139">INPUTS</span></span>

### <span data-ttu-id="f9e70-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f9e70-140">System.String</span></span>

## <span data-ttu-id="f9e70-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f9e70-141">OUTPUTS</span></span>

### <span data-ttu-id="f9e70-142">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f9e70-142">None</span></span>

## <span data-ttu-id="f9e70-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f9e70-143">NOTES</span></span>

## <span data-ttu-id="f9e70-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f9e70-144">RELATED LINKS</span></span>

[<span data-ttu-id="f9e70-145">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="f9e70-145">Get-AzDataLakeStoreDeletedItem</span></span>](./Get-AzDataLakeStoreDeletedItem.md)