---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/enable-azurestoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Enable-AzureStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Enable-AzureStorageDeleteRetentionPolicy.md
ms.openlocfilehash: 4778e0230cd50b3567cb0ded2ca629cd81db33fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587365"
---
# <span data-ttu-id="54564-101">Enable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="54564-101">Enable-AzureStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="54564-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54564-102">SYNOPSIS</span></span>
<span data-ttu-id="54564-103">Azure depolama blob hizmeti için bekletme ilkesini silme özelliğini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="54564-103">Enable delete retention policy  for the Azure Storage Blob service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54564-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="54564-104">SYNTAX</span></span>

```
Enable-AzureStorageDeleteRetentionPolicy [-RetentionDays] <Int32> [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54564-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="54564-105">DESCRIPTION</span></span>
<span data-ttu-id="54564-106">**Enable-AzureStorageDeleteRetentionPolicy** cmdlet 'ı Azure depolama blob hizmeti için bekletme ilkesini silmeye olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="54564-106">The **Enable-AzureStorageDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="54564-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="54564-107">EXAMPLES</span></span>

### <span data-ttu-id="54564-108">Örnek 1: blob hizmeti için bekletme ilkesini silme özelliğini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="54564-108">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzureStorageDeleteRetentionPolicy -RetentionDays 3
```

<span data-ttu-id="54564-109">Bu komut, blob hizmeti için bekletme ilkesini silme</span><span class="sxs-lookup"><span data-stu-id="54564-109">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 3.</span></span>

## <span data-ttu-id="54564-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="54564-110">PARAMETERS</span></span>

### <span data-ttu-id="54564-111">-Context</span><span class="sxs-lookup"><span data-stu-id="54564-111">-Context</span></span>
<span data-ttu-id="54564-112">Azure depolama bağlamı nesnesi</span><span class="sxs-lookup"><span data-stu-id="54564-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="54564-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54564-113">-DefaultProfile</span></span>
<span data-ttu-id="54564-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="54564-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54564-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="54564-115">-PassThru</span></span>
<span data-ttu-id="54564-116">DeleteRetentionPolicyProperties görüntüleme</span><span class="sxs-lookup"><span data-stu-id="54564-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="54564-117">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="54564-117">-RetentionDays</span></span>
<span data-ttu-id="54564-118">KayıtSayısı için bekletme günü sayısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="54564-118">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Days

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54564-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="54564-119">-Confirm</span></span>
<span data-ttu-id="54564-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="54564-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54564-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54564-121">-WhatIf</span></span>
<span data-ttu-id="54564-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="54564-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54564-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="54564-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54564-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54564-124">CommonParameters</span></span>
<span data-ttu-id="54564-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="54564-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54564-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54564-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54564-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="54564-127">INPUTS</span></span>

### <span data-ttu-id="54564-128">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="54564-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="54564-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="54564-129">OUTPUTS</span></span>

### <span data-ttu-id="54564-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="54564-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="54564-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="54564-131">NOTES</span></span>

## <span data-ttu-id="54564-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="54564-132">RELATED LINKS</span></span>
