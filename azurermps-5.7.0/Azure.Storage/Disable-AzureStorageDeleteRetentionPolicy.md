---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/disable-azurestoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Disable-AzureStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Disable-AzureStorageDeleteRetentionPolicy.md
ms.openlocfilehash: d3de0cc49eb0e36572daa9e4cfbbb41c0db0936a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762182"
---
# <span data-ttu-id="89a2c-101">Disable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="89a2c-101">Disable-AzureStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="89a2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89a2c-102">SYNOPSIS</span></span>
<span data-ttu-id="89a2c-103">Azure depolama blob hizmeti için bekletme ilkesini Sil 'i devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="89a2c-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89a2c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="89a2c-104">SYNTAX</span></span>

```
Disable-AzureStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="89a2c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="89a2c-105">DESCRIPTION</span></span>
<span data-ttu-id="89a2c-106">**Disable-AzureStorageDeleteRetentionPolicy** cmdlet 'ı Azure depolama blob hizmeti için bekletme ilkesini silme işlemini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="89a2c-106">The **Disable-AzureStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="89a2c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="89a2c-107">EXAMPLES</span></span>

### <span data-ttu-id="89a2c-108">Örnek 1: blob hizmeti için bekletme ilkesini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="89a2c-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzureStorageDeleteRetentionPolicy
```

<span data-ttu-id="89a2c-109">Bu komut, blob hizmeti için bekletme ilkesini silme özelliğini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="89a2c-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="89a2c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="89a2c-110">PARAMETERS</span></span>

### <span data-ttu-id="89a2c-111">-Context</span><span class="sxs-lookup"><span data-stu-id="89a2c-111">-Context</span></span>
<span data-ttu-id="89a2c-112">Azure depolama bağlamı nesnesi</span><span class="sxs-lookup"><span data-stu-id="89a2c-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="89a2c-113">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="89a2c-113">-PassThru</span></span>
<span data-ttu-id="89a2c-114">DeleteRetentionPolicyProperties görüntüleme</span><span class="sxs-lookup"><span data-stu-id="89a2c-114">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="89a2c-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="89a2c-115">-Confirm</span></span>
<span data-ttu-id="89a2c-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="89a2c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89a2c-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89a2c-117">-WhatIf</span></span>
<span data-ttu-id="89a2c-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="89a2c-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89a2c-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="89a2c-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89a2c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89a2c-120">CommonParameters</span></span>
<span data-ttu-id="89a2c-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="89a2c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89a2c-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89a2c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89a2c-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="89a2c-123">INPUTS</span></span>

### <span data-ttu-id="89a2c-124">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="89a2c-124">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="89a2c-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="89a2c-125">OUTPUTS</span></span>

### <span data-ttu-id="89a2c-126">Microsoft. Windowsazde. Commands. Storage. model. ResourceMode. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="89a2c-126">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceMode.PSSeriviceProperties</span></span>

## <span data-ttu-id="89a2c-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="89a2c-127">NOTES</span></span>

## <span data-ttu-id="89a2c-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="89a2c-128">RELATED LINKS</span></span>

