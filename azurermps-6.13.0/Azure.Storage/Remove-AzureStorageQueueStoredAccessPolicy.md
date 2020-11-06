---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 1f5c97824a9296954f2c7bad742b5f8176359563
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592838"
---
# <span data-ttu-id="1e421-101">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1e421-101">Remove-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="1e421-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e421-102">SYNOPSIS</span></span>
<span data-ttu-id="1e421-103">Depolanan bir Access ilkesini Azure depolama sırasından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1e421-103">Removes a stored access policy from an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e421-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1e421-104">SYNTAX</span></span>

```
Remove-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1e421-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1e421-105">DESCRIPTION</span></span>
<span data-ttu-id="1e421-106">**Remove-AzureStorageQueueStoredAccessPolicy** cmdlet 'i Azure depolama sırasından depolanan bir Access ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1e421-106">The **Remove-AzureStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="1e421-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1e421-107">EXAMPLES</span></span>

### <span data-ttu-id="1e421-108">Örnek 1: depolanan bir erişim ilkesini depolama sırasından kaldırma</span><span class="sxs-lookup"><span data-stu-id="1e421-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="1e421-109">Bu komut, Policy04 adındaki bir erişim ilkesini MyQueue adındaki depolama sırasından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1e421-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="1e421-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1e421-110">PARAMETERS</span></span>

### <span data-ttu-id="1e421-111">-Context</span><span class="sxs-lookup"><span data-stu-id="1e421-111">-Context</span></span>
<span data-ttu-id="1e421-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e421-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="1e421-113">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="1e421-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="1e421-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e421-114">-DefaultProfile</span></span>
<span data-ttu-id="1e421-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1e421-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e421-116">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1e421-116">-PassThru</span></span>
<span data-ttu-id="1e421-117">Bu cmdlet 'in işlemin başarısını yansıtan bir **Boole değeri** döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="1e421-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="1e421-118">Varsayılan olarak, bu cmdlet değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="1e421-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="1e421-119">-İlke</span><span class="sxs-lookup"><span data-stu-id="1e421-119">-Policy</span></span>
<span data-ttu-id="1e421-120">Bu cmdlet 'in kaldırdığı depolanan erişim ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e421-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e421-121">-Sıra</span><span class="sxs-lookup"><span data-stu-id="1e421-121">-Queue</span></span>
<span data-ttu-id="1e421-122">Azure depolama sırası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1e421-122">Specifies the Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e421-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="1e421-123">-Confirm</span></span>
<span data-ttu-id="1e421-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1e421-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e421-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e421-125">-WhatIf</span></span>
<span data-ttu-id="1e421-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1e421-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e421-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1e421-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e421-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e421-128">CommonParameters</span></span>
<span data-ttu-id="1e421-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1e421-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e421-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e421-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e421-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1e421-131">INPUTS</span></span>

### <span data-ttu-id="1e421-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1e421-132">System.String</span></span>

### <span data-ttu-id="1e421-133">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="1e421-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1e421-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1e421-134">OUTPUTS</span></span>

### <span data-ttu-id="1e421-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1e421-135">System.Boolean</span></span>

## <span data-ttu-id="1e421-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1e421-136">NOTES</span></span>

## <span data-ttu-id="1e421-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1e421-137">RELATED LINKS</span></span>

[<span data-ttu-id="1e421-138">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1e421-138">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="1e421-139">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="1e421-139">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="1e421-140">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1e421-140">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="1e421-141">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1e421-141">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)
