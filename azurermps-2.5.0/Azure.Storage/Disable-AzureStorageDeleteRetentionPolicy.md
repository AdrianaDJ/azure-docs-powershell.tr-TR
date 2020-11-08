---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/disable-azurestoragedeleteretentionpolicy
schema: 2.0.0
ms.openlocfilehash: d899b34e2f880a0351ce4d10f360f7bc29011b0c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939451"
---
# <span data-ttu-id="24289-101">Disable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="24289-101">Disable-AzureStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="24289-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24289-102">SYNOPSIS</span></span>
<span data-ttu-id="24289-103">Azure depolama blob hizmeti için bekletme ilkesini Sil 'i devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="24289-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24289-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="24289-104">SYNTAX</span></span>

```
Disable-AzureStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24289-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="24289-105">DESCRIPTION</span></span>
<span data-ttu-id="24289-106">**Disable-AzureStorageDeleteRetentionPolicy** cmdlet 'ı Azure depolama blob hizmeti için bekletme ilkesini silme işlemini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="24289-106">The **Disable-AzureStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="24289-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="24289-107">EXAMPLES</span></span>

### <span data-ttu-id="24289-108">Örnek 1: blob hizmeti için bekletme ilkesini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="24289-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzureStorageDeleteRetentionPolicy
```

<span data-ttu-id="24289-109">Bu komut, blob hizmeti için bekletme ilkesini silme özelliğini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="24289-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="24289-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="24289-110">PARAMETERS</span></span>

### <span data-ttu-id="24289-111">-Context</span><span class="sxs-lookup"><span data-stu-id="24289-111">-Context</span></span>
<span data-ttu-id="24289-112">Azure depolama bağlamı nesnesi</span><span class="sxs-lookup"><span data-stu-id="24289-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="24289-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24289-113">-DefaultProfile</span></span>
<span data-ttu-id="24289-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="24289-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24289-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="24289-115">-PassThru</span></span>
<span data-ttu-id="24289-116">DeleteRetentionPolicyProperties görüntüleme</span><span class="sxs-lookup"><span data-stu-id="24289-116">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="24289-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="24289-117">-Confirm</span></span>
<span data-ttu-id="24289-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="24289-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24289-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24289-119">-WhatIf</span></span>
<span data-ttu-id="24289-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="24289-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24289-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="24289-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24289-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24289-122">CommonParameters</span></span>
<span data-ttu-id="24289-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="24289-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24289-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24289-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24289-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="24289-125">INPUTS</span></span>

### <span data-ttu-id="24289-126">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="24289-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="24289-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="24289-127">OUTPUTS</span></span>

### <span data-ttu-id="24289-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="24289-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="24289-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="24289-129">NOTES</span></span>

## <span data-ttu-id="24289-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="24289-130">RELATED LINKS</span></span>