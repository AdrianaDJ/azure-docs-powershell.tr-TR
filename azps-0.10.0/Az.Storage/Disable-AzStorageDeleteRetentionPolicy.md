---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: f09ba3cdd0404f1eca21540a6893f1bcd67f05e5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936290"
---
# <span data-ttu-id="8bbf6-101">Disable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8bbf6-101">Disable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="8bbf6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bbf6-102">SYNOPSIS</span></span>
<span data-ttu-id="8bbf6-103">Azure depolama blob hizmeti için bekletme ilkesini Sil 'i devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="8bbf6-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="8bbf6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8bbf6-104">SYNTAX</span></span>

```
Disable-AzStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bbf6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8bbf6-105">DESCRIPTION</span></span>
<span data-ttu-id="8bbf6-106">**Disable-AzStorageDeleteRetentionPolicy** cmdlet 'ı Azure depolama blob hizmeti için bekletme ilkesini silme işlemini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="8bbf6-106">The **Disable-AzStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="8bbf6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8bbf6-107">EXAMPLES</span></span>

### <span data-ttu-id="8bbf6-108">Örnek 1: blob hizmeti için bekletme ilkesini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="8bbf6-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageDeleteRetentionPolicy
```

<span data-ttu-id="8bbf6-109">Bu komut, blob hizmeti için bekletme ilkesini silme özelliğini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="8bbf6-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="8bbf6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8bbf6-110">PARAMETERS</span></span>

### <span data-ttu-id="8bbf6-111">-Context</span><span class="sxs-lookup"><span data-stu-id="8bbf6-111">-Context</span></span>
<span data-ttu-id="8bbf6-112">Azure depolama bağlamı nesnesi</span><span class="sxs-lookup"><span data-stu-id="8bbf6-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="8bbf6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bbf6-113">-DefaultProfile</span></span>
<span data-ttu-id="8bbf6-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8bbf6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bbf6-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="8bbf6-115">-PassThru</span></span>
<span data-ttu-id="8bbf6-116">DeleteRetentionPolicyProperties görüntüleme</span><span class="sxs-lookup"><span data-stu-id="8bbf6-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="8bbf6-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="8bbf6-117">-Confirm</span></span>
<span data-ttu-id="8bbf6-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8bbf6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bbf6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bbf6-119">-WhatIf</span></span>
<span data-ttu-id="8bbf6-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8bbf6-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bbf6-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8bbf6-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bbf6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bbf6-122">CommonParameters</span></span>
<span data-ttu-id="8bbf6-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8bbf6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bbf6-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bbf6-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bbf6-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8bbf6-125">INPUTS</span></span>

### <span data-ttu-id="8bbf6-126">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="8bbf6-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8bbf6-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8bbf6-127">OUTPUTS</span></span>

### <span data-ttu-id="8bbf6-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8bbf6-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="8bbf6-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8bbf6-129">NOTES</span></span>

## <span data-ttu-id="8bbf6-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8bbf6-130">RELATED LINKS</span></span>