---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: 36176b16fab75b24549ceeb3d107114632703129
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096729"
---
# <span data-ttu-id="ae50a-101">Enable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ae50a-101">Enable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="ae50a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae50a-102">SYNOPSIS</span></span>
<span data-ttu-id="ae50a-103">Azure depolama blob hizmeti için bekletme ilkesini silme özelliğini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="ae50a-103">Enable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="ae50a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ae50a-104">SYNTAX</span></span>

```
Enable-AzStorageDeleteRetentionPolicy [-RetentionDays] <Int32> [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae50a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ae50a-105">DESCRIPTION</span></span>
<span data-ttu-id="ae50a-106">**Enable-AzStorageDeleteRetentionPolicy** cmdlet 'ı Azure depolama blob hizmeti için bekletme ilkesini silmeye olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="ae50a-106">The **Enable-AzStorageDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="ae50a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ae50a-107">EXAMPLES</span></span>

### <span data-ttu-id="ae50a-108">Örnek 1: blob hizmeti için bekletme ilkesini silme özelliğini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="ae50a-108">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzStorageDeleteRetentionPolicy -RetentionDays 3
```

<span data-ttu-id="ae50a-109">Bu komut, blob hizmeti için bekletme ilkesini silme</span><span class="sxs-lookup"><span data-stu-id="ae50a-109">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 3.</span></span>

## <span data-ttu-id="ae50a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ae50a-110">PARAMETERS</span></span>

### <span data-ttu-id="ae50a-111">-Context</span><span class="sxs-lookup"><span data-stu-id="ae50a-111">-Context</span></span>
<span data-ttu-id="ae50a-112">Azure depolama bağlamı nesnesi</span><span class="sxs-lookup"><span data-stu-id="ae50a-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="ae50a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae50a-113">-DefaultProfile</span></span>
<span data-ttu-id="ae50a-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ae50a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae50a-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ae50a-115">-PassThru</span></span>
<span data-ttu-id="ae50a-116">DeleteRetentionPolicyProperties görüntüleme</span><span class="sxs-lookup"><span data-stu-id="ae50a-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="ae50a-117">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="ae50a-117">-RetentionDays</span></span>
<span data-ttu-id="ae50a-118">KayıtSayısı için bekletme günü sayısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ae50a-118">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

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

### <span data-ttu-id="ae50a-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="ae50a-119">-Confirm</span></span>
<span data-ttu-id="ae50a-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ae50a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae50a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae50a-121">-WhatIf</span></span>
<span data-ttu-id="ae50a-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ae50a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae50a-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ae50a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae50a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae50a-124">CommonParameters</span></span>
<span data-ttu-id="ae50a-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ae50a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae50a-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae50a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae50a-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ae50a-127">INPUTS</span></span>

### <span data-ttu-id="ae50a-128">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="ae50a-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ae50a-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ae50a-129">OUTPUTS</span></span>

### <span data-ttu-id="ae50a-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ae50a-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="ae50a-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ae50a-131">NOTES</span></span>

## <span data-ttu-id="ae50a-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ae50a-132">RELATED LINKS</span></span>
