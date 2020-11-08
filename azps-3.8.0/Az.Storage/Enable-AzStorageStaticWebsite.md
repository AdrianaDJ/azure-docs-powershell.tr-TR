---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageStaticWebsite.md
ms.openlocfilehash: e97e89c1ab7160f1eb06c9c94cd5620a48b0463e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097784"
---
# <span data-ttu-id="745b7-101">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="745b7-101">Enable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="745b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="745b7-102">SYNOPSIS</span></span>
<span data-ttu-id="745b7-103">Azure depolama hesabı için statik Web sitesini etkinleştirme.</span><span class="sxs-lookup"><span data-stu-id="745b7-103">Enable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="745b7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="745b7-104">SYNTAX</span></span>

```
Enable-AzStorageStaticWebsite [[-IndexDocument] <String>] [[-ErrorDocument404Path] <String>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="745b7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="745b7-105">DESCRIPTION</span></span>
<span data-ttu-id="745b7-106">**Enable-AzStorageStaticWebsite** cmdlet 'ı Azure depolama hesabı için statik Web sitesini etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="745b7-106">The **Enable-AzStorageStaticWebsite** cmdlet enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="745b7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="745b7-107">EXAMPLES</span></span>

### <span data-ttu-id="745b7-108">Örnek 1: Azure depolama hesabı için statik Web sitesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="745b7-108">Example 1: Enable static website for the Azure Storage account</span></span>
```
C:\PS>Enable-AzStorageStaticWebsite -IndexDocument $indexdoc -ErrorDocument404Path $errordoc
```

<span data-ttu-id="745b7-109">Bu komut Azure depolama hesabı için statik Web sitesini etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="745b7-109">This command enables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="745b7-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="745b7-110">PARAMETERS</span></span>

### <span data-ttu-id="745b7-111">-Context</span><span class="sxs-lookup"><span data-stu-id="745b7-111">-Context</span></span>
<span data-ttu-id="745b7-112">Azure depolama bağlamı nesnesi</span><span class="sxs-lookup"><span data-stu-id="745b7-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="745b7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="745b7-113">-DefaultProfile</span></span>
<span data-ttu-id="745b7-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="745b7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="745b7-115">-ErrorDocument404Path</span><span class="sxs-lookup"><span data-stu-id="745b7-115">-ErrorDocument404Path</span></span>
<span data-ttu-id="745b7-116">404 verildiğinde gösterilmesi gereken hata belgesinin yolu (yani, bir tarayıcı varolmayan bir sayfayı istediğinde.)</span><span class="sxs-lookup"><span data-stu-id="745b7-116">The path to the error document that should be shown when a 404 is issued (meaning, when a browser requests a page that does not exist.)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="745b7-117">-IndexDocument</span><span class="sxs-lookup"><span data-stu-id="745b7-117">-IndexDocument</span></span>
<span data-ttu-id="745b7-118">Her dizindeki Dizin belgesinin adı.</span><span class="sxs-lookup"><span data-stu-id="745b7-118">The name of the index document in each directory.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="745b7-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="745b7-119">-PassThru</span></span>
<span data-ttu-id="745b7-120">ServiceProperties 'te statik Web sitesi ayarını görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="745b7-120">Display Static Website setting in ServiceProperties.</span></span>

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

### <span data-ttu-id="745b7-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="745b7-121">-Confirm</span></span>
<span data-ttu-id="745b7-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="745b7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="745b7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="745b7-123">-WhatIf</span></span>
<span data-ttu-id="745b7-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="745b7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="745b7-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="745b7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="745b7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="745b7-126">CommonParameters</span></span>
<span data-ttu-id="745b7-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="745b7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="745b7-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="745b7-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="745b7-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="745b7-129">INPUTS</span></span>

### <span data-ttu-id="745b7-130">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="745b7-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="745b7-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="745b7-131">OUTPUTS</span></span>

### <span data-ttu-id="745b7-132">Microsoft. Windowsazme. Commands. Storage. model. ResourceModel. PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="745b7-132">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="745b7-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="745b7-133">NOTES</span></span>

## <span data-ttu-id="745b7-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="745b7-134">RELATED LINKS</span></span>