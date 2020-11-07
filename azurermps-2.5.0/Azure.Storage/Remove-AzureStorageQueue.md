---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragequeue
schema: 2.0.0
ms.openlocfilehash: e2fcfa1d100f460bcf352cc26fd0e094d52cad21
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939428"
---
# <span data-ttu-id="a0188-101">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="a0188-101">Remove-AzureStorageQueue</span></span>

## <span data-ttu-id="a0188-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0188-102">SYNOPSIS</span></span>
<span data-ttu-id="a0188-103">Depolama kuyruğunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a0188-103">Removes a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0188-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a0188-104">SYNTAX</span></span>

```
Remove-AzureStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0188-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a0188-105">DESCRIPTION</span></span>
<span data-ttu-id="a0188-106">**Remove-AzureStorageQueue** cmdlet 'i bir depolama sırasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a0188-106">The **Remove-AzureStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="a0188-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a0188-107">EXAMPLES</span></span>

### <span data-ttu-id="a0188-108">Örnek 1: depolama kuyruğunu ada göre kaldırma</span><span class="sxs-lookup"><span data-stu-id="a0188-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzureStorageQueue "ContosoQueue01"
```

<span data-ttu-id="a0188-109">Bu komut, ContosoQueue01 adlı bir sırayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a0188-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="a0188-110">Örnek 2: birden çok depolama sırasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="a0188-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue "Contoso*" | Remove-AzureStorageQueue
```

<span data-ttu-id="a0188-111">Bu komut, contoso ile başlayan tüm sıraları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a0188-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="a0188-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a0188-112">PARAMETERS</span></span>

### <span data-ttu-id="a0188-113">-Context</span><span class="sxs-lookup"><span data-stu-id="a0188-113">-Context</span></span>
<span data-ttu-id="a0188-114">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0188-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="a0188-115">Depolama bağlamını edinmek için New-AzureStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0188-115">To obtain the storage context, the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a0188-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0188-116">-DefaultProfile</span></span>
<span data-ttu-id="a0188-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a0188-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0188-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a0188-118">-Force</span></span>
<span data-ttu-id="a0188-119">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="a0188-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a0188-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="a0188-120">-Name</span></span>
<span data-ttu-id="a0188-121">Kaldırılacak sıranın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0188-121">Specifies the name of the queue to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0188-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a0188-122">-PassThru</span></span>
<span data-ttu-id="a0188-123">Bu cmdlet 'in işlemin başarısını yansıtan bir **Boole değeri** döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="a0188-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="a0188-124">Varsayılan olarak, bu cmdlet değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="a0188-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="a0188-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="a0188-125">-Confirm</span></span>
<span data-ttu-id="a0188-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a0188-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0188-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0188-127">-WhatIf</span></span>
<span data-ttu-id="a0188-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a0188-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0188-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a0188-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0188-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0188-130">CommonParameters</span></span>
<span data-ttu-id="a0188-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a0188-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0188-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0188-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0188-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a0188-133">INPUTS</span></span>

### <span data-ttu-id="a0188-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a0188-134">System.String</span></span>

### <span data-ttu-id="a0188-135">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="a0188-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a0188-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a0188-136">OUTPUTS</span></span>

### <span data-ttu-id="a0188-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a0188-137">System.Boolean</span></span>

## <span data-ttu-id="a0188-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a0188-138">NOTES</span></span>

## <span data-ttu-id="a0188-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a0188-139">RELATED LINKS</span></span>

[<span data-ttu-id="a0188-140">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="a0188-140">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="a0188-141">Yeni-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="a0188-141">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)
