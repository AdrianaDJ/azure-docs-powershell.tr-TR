---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/enable-azurestoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Enable-AzureStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Enable-AzureStorageDeleteRetentionPolicy.md
ms.openlocfilehash: f8303a9d87a2bd5312732bd01eb3d42bd1e0a285
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587729"
---
# <span data-ttu-id="79fc5-101">Enable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="79fc5-101">Enable-AzureStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="79fc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79fc5-102">SYNOPSIS</span></span>
<span data-ttu-id="79fc5-103">Azure depolama blob hizmeti için bekletme ilkesini silme özelliğini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="79fc5-103">Enable delete retention policy  for the Azure Storage Blob service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79fc5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="79fc5-104">SYNTAX</span></span>

```
Enable-AzureStorageDeleteRetentionPolicy [-RetentionDays] <Int32> [-PassThru] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79fc5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="79fc5-105">DESCRIPTION</span></span>
<span data-ttu-id="79fc5-106">**Enable-AzureStorageDeleteRetentionPolicy** cmdlet 'ı Azure depolama blob hizmeti için bekletme ilkesini silmeye olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="79fc5-106">The **Enable-AzureStorageDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="79fc5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="79fc5-107">EXAMPLES</span></span>

### <span data-ttu-id="79fc5-108">Örnek 1: blob hizmeti için bekletme ilkesini silme özelliğini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="79fc5-108">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzureStorageDeleteRetentionPolicy -RetentionDays 3
```

<span data-ttu-id="79fc5-109">Bu komut, blob hizmeti için bekletme ilkesini silme</span><span class="sxs-lookup"><span data-stu-id="79fc5-109">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 3.</span></span>

## <span data-ttu-id="79fc5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="79fc5-110">PARAMETERS</span></span>

### <span data-ttu-id="79fc5-111">-Context</span><span class="sxs-lookup"><span data-stu-id="79fc5-111">-Context</span></span>
<span data-ttu-id="79fc5-112">Azure depolama bağlamı nesnesi</span><span class="sxs-lookup"><span data-stu-id="79fc5-112">Azure Storage Context Object</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79fc5-113">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="79fc5-113">-PassThru</span></span>
<span data-ttu-id="79fc5-114">DeleteRetentionPolicyProperties görüntüleme</span><span class="sxs-lookup"><span data-stu-id="79fc5-114">Display DeleteRetentionPolicyProperties</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79fc5-115">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="79fc5-115">-RetentionDays</span></span>
<span data-ttu-id="79fc5-116">KayıtSayısı için bekletme günü sayısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="79fc5-116">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: Days

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79fc5-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="79fc5-117">-Confirm</span></span>
<span data-ttu-id="79fc5-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="79fc5-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79fc5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79fc5-119">-WhatIf</span></span>
<span data-ttu-id="79fc5-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="79fc5-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79fc5-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="79fc5-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79fc5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79fc5-122">CommonParameters</span></span>
<span data-ttu-id="79fc5-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="79fc5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79fc5-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79fc5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79fc5-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="79fc5-125">INPUTS</span></span>

### <span data-ttu-id="79fc5-126">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="79fc5-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="79fc5-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="79fc5-127">OUTPUTS</span></span>

### <span data-ttu-id="79fc5-128">Microsoft. Windowsazma. Storage. Shared. Protocol. DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="79fc5-128">Microsoft.WindowsAzure.Storage.Shared.Protocol.DeleteRetentionPolicyProperties</span></span>

## <span data-ttu-id="79fc5-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="79fc5-129">NOTES</span></span>

## <span data-ttu-id="79fc5-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="79fc5-130">RELATED LINKS</span></span>

