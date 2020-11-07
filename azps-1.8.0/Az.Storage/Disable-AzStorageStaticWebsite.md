---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragestaticwebsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageStaticWebsite.md
ms.openlocfilehash: 4d5a12136dc23375e7ac5ea822c663c018f3bf68
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758701"
---
# <span data-ttu-id="6bc46-101">Disable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="6bc46-101">Disable-AzStorageStaticWebsite</span></span>

## <span data-ttu-id="6bc46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bc46-102">SYNOPSIS</span></span>
<span data-ttu-id="6bc46-103">Azure depolama hesabı için statik Web sitesini devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="6bc46-103">Disable static website for the Azure Storage account.</span></span>

## <span data-ttu-id="6bc46-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6bc46-104">SYNTAX</span></span>

```
Disable-AzStorageStaticWebsite [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bc46-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6bc46-105">DESCRIPTION</span></span>
<span data-ttu-id="6bc46-106">**Disable-AzStorageStaticWebsite** cmdlet 'ı, Azure depolama hesabı için statik Web sitesini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="6bc46-106">The **Disable-AzStorageStaticWebsite** cmdlet disables static website for the Azure Storage account.</span></span>

## <span data-ttu-id="6bc46-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6bc46-107">EXAMPLES</span></span>

### <span data-ttu-id="6bc46-108">Örnek 1: Azure depolama hesabı için statik Web sitesini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="6bc46-108">Example 1: Disable static website for a Azure Storage account</span></span>
```
C:\PS>Disable-AzStorageStaticWebsite
```

<span data-ttu-id="6bc46-109">Bu komut, Azure depolama hesabı için statik Web sitesini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="6bc46-109">This command disables static website for a Azure Storage account.</span></span>

## <span data-ttu-id="6bc46-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6bc46-110">PARAMETERS</span></span>

### <span data-ttu-id="6bc46-111">-Context</span><span class="sxs-lookup"><span data-stu-id="6bc46-111">-Context</span></span>
<span data-ttu-id="6bc46-112">Azure depolama bağlamı nesnesi</span><span class="sxs-lookup"><span data-stu-id="6bc46-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="6bc46-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bc46-113">-DefaultProfile</span></span>
<span data-ttu-id="6bc46-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6bc46-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bc46-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6bc46-115">-PassThru</span></span>
<span data-ttu-id="6bc46-116">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="6bc46-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6bc46-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="6bc46-117">-Confirm</span></span>
<span data-ttu-id="6bc46-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6bc46-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bc46-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bc46-119">-WhatIf</span></span>
<span data-ttu-id="6bc46-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6bc46-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bc46-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6bc46-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bc46-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bc46-122">CommonParameters</span></span>
<span data-ttu-id="6bc46-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6bc46-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bc46-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bc46-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bc46-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6bc46-125">INPUTS</span></span>

### <span data-ttu-id="6bc46-126">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="6bc46-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6bc46-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6bc46-127">OUTPUTS</span></span>

### <span data-ttu-id="6bc46-128">Microsoft. Windowsazme. Commands. Storage. model. ResourceModel. PSStaticWebsiteProperties</span><span class="sxs-lookup"><span data-stu-id="6bc46-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSStaticWebsiteProperties</span></span>

## <span data-ttu-id="6bc46-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6bc46-129">NOTES</span></span>

## <span data-ttu-id="6bc46-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6bc46-130">RELATED LINKS</span></span>
