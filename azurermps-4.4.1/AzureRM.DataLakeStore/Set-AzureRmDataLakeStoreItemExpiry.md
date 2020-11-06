---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
ms.openlocfilehash: f71c26e69f9f297a23d4e6902ca6aaac6b135c42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595178"
---
# <span data-ttu-id="abb68-101">Set-AzureRmDataLakeStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="abb68-101">Set-AzureRmDataLakeStoreItemExpiry</span></span>

## <span data-ttu-id="abb68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abb68-102">SYNOPSIS</span></span>
<span data-ttu-id="abb68-103">Azure Data Lake Store hesabındaki bir dosyanın süresi bitim süresini ayarlar veya kaldırır.</span><span class="sxs-lookup"><span data-stu-id="abb68-103">Sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abb68-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="abb68-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="abb68-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="abb68-105">DESCRIPTION</span></span>
<span data-ttu-id="abb68-106">**Set-AzureRmDataLakeStoreItemExpiry** cmdlet 'ı, Azure Data Lake Store hesabındaki bir dosyanın süresi bitim süresini ayarlar veya kaldırır.</span><span class="sxs-lookup"><span data-stu-id="abb68-106">The **Set-AzureRmDataLakeStoreItemExpiry** cmdlet sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="abb68-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="abb68-107">EXAMPLES</span></span>

### <span data-ttu-id="abb68-108">Örnek 1: dosya için son kullanma zamanını ayarlama</span><span class="sxs-lookup"><span data-stu-id="abb68-108">Example 1: Set the expiration time for a file</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

<span data-ttu-id="abb68-109">Şu andan itibaren, ContosoADL hesabındaki myfile.txt zaman aşımı süresini iki saat olacak şekilde ayarlar.</span><span class="sxs-lookup"><span data-stu-id="abb68-109">Sets expiration on the file myfile.txt in account ContosoADL to be two hours from now.</span></span>
<span data-ttu-id="abb68-110">Bu, dosyanın süresi dolmasına neden olur (silme için işaretlenir) iki saat içinde.</span><span class="sxs-lookup"><span data-stu-id="abb68-110">This will cause the file to expire (be marked for delete) in two hours.</span></span>

### <span data-ttu-id="abb68-111">Örnek 2: dosyanın süre sonunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="abb68-111">Example 2: Remove the expiration on a file</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

<span data-ttu-id="abb68-112">' ContosoADL ' hesabında ' myfile.txt ' dosyasında daha önce ayarlanmış olan sona erdirmeyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="abb68-112">Removes any expiration that was previously set on file 'myfile.txt' in account 'ContosoADL'.</span></span>
<span data-ttu-id="abb68-113">Bu, dosyanın otomatik olarak süresinin dolamayacağı anlamına gelir (silme için işaretlenir) ve el ile silinmesi veya yeniden kullanım süresi olarak ayarlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="abb68-113">This means the file will not automatically expire (be marked for delete) and will need to be manually deleted or set to expire again.</span></span>

## <span data-ttu-id="abb68-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="abb68-114">PARAMETERS</span></span>

### <span data-ttu-id="abb68-115">-Hesap</span><span class="sxs-lookup"><span data-stu-id="abb68-115">-Account</span></span>
<span data-ttu-id="abb68-116">Data Lake Store hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="abb68-116">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="abb68-117">-Süre sonu</span><span class="sxs-lookup"><span data-stu-id="abb68-117">-Expiration</span></span>
<span data-ttu-id="abb68-118">Belirtilen dosyanın mutlak son kullanma tarihi.</span><span class="sxs-lookup"><span data-stu-id="abb68-118">The absolute expiration time for the specified file.</span></span>
<span data-ttu-id="abb68-119">Değer yoksa veya MaxValue olarak ayarlanmamışsa, dosyanın süresi dolmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="abb68-119">If no value or set to MaxValue, the file will never expire.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abb68-120">-Yol</span><span class="sxs-lookup"><span data-stu-id="abb68-120">-Path</span></span>
<span data-ttu-id="abb68-121">Bitiş tarihi ayarlanacak veya kaldırılacak dosya öğesinin veri Lake Store yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="abb68-121">Specifies the Data Lake Store path of the file item for which to set or remove expiry.</span></span>

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

### <span data-ttu-id="abb68-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="abb68-122">-Confirm</span></span>
<span data-ttu-id="abb68-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="abb68-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abb68-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abb68-124">-WhatIf</span></span>
<span data-ttu-id="abb68-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="abb68-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abb68-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="abb68-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abb68-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abb68-127">-DefaultProfile</span></span>
<span data-ttu-id="abb68-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="abb68-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abb68-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abb68-129">CommonParameters</span></span>
<span data-ttu-id="abb68-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="abb68-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abb68-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abb68-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abb68-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="abb68-132">INPUTS</span></span>

## <span data-ttu-id="abb68-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="abb68-133">OUTPUTS</span></span>

### <span data-ttu-id="abb68-134">DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="abb68-134">DataLakeStoreItem</span></span>
<span data-ttu-id="abb68-135">Yeni son kullanma tarihi olan güncelleştirilmiş dosya.</span><span class="sxs-lookup"><span data-stu-id="abb68-135">The updated file with a new expiration time.</span></span>

## <span data-ttu-id="abb68-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="abb68-136">NOTES</span></span>
<span data-ttu-id="abb68-137">Diğer ad: Set-AdlStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="abb68-137">Alias: Set-AdlStoreItemExpiry</span></span>

## <span data-ttu-id="abb68-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="abb68-138">RELATED LINKS</span></span>

[<span data-ttu-id="abb68-139">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="abb68-139">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

