---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: ''
schema: 2.0.0
ms.openlocfilehash: 116dcc8967ab18d0b67cd3e4eeea91190c38930f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572257"
---
# <span data-ttu-id="ddd5e-101">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ddd5e-101">Remove-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="ddd5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddd5e-102">SYNOPSIS</span></span>
<span data-ttu-id="ddd5e-103">Depolanan bir Access ilkesini Azure depolama sırasından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ddd5e-103">Removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="ddd5e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ddd5e-104">SYNTAX</span></span>

```
Remove-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddd5e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ddd5e-105">DESCRIPTION</span></span>
<span data-ttu-id="ddd5e-106">**Remove-AzureStorageQueueStoredAccessPolicy** cmdlet 'i Azure depolama sırasından depolanan bir Access ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ddd5e-106">The **Remove-AzureStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="ddd5e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ddd5e-107">EXAMPLES</span></span>

### <span data-ttu-id="ddd5e-108">Örnek 1: depolanan bir erişim ilkesini depolama sırasından kaldırma</span><span class="sxs-lookup"><span data-stu-id="ddd5e-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="ddd5e-109">Bu komut, Policy04 adındaki bir erişim ilkesini MyQueue adındaki depolama sırasından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ddd5e-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="ddd5e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ddd5e-110">PARAMETERS</span></span>

### <span data-ttu-id="ddd5e-111">-Context</span><span class="sxs-lookup"><span data-stu-id="ddd5e-111">-Context</span></span>
<span data-ttu-id="ddd5e-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddd5e-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ddd5e-113">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ddd5e-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ddd5e-114">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ddd5e-114">-PassThru</span></span>
<span data-ttu-id="ddd5e-115">Bu cmdlet 'in işlemin başarısını yansıtan bir **Boole değeri** döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="ddd5e-115">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="ddd5e-116">Varsayılan olarak, bu cmdlet değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="ddd5e-116">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="ddd5e-117">-İlke</span><span class="sxs-lookup"><span data-stu-id="ddd5e-117">-Policy</span></span>
<span data-ttu-id="ddd5e-118">Bu paylaşılan erişim Imzası (SAS) belirtecinin izinlerini içeren depolanan erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddd5e-118">Specifies the stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd5e-119">-Sıra</span><span class="sxs-lookup"><span data-stu-id="ddd5e-119">-Queue</span></span>
<span data-ttu-id="ddd5e-120">Azure depolama sırası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddd5e-120">Specifies the Azure storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd5e-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="ddd5e-121">-Confirm</span></span>
<span data-ttu-id="ddd5e-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ddd5e-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd5e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddd5e-123">-WhatIf</span></span>
<span data-ttu-id="ddd5e-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ddd5e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddd5e-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ddd5e-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddd5e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddd5e-126">CommonParameters</span></span>
<span data-ttu-id="ddd5e-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ddd5e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddd5e-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddd5e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddd5e-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ddd5e-129">INPUTS</span></span>

## <span data-ttu-id="ddd5e-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ddd5e-130">OUTPUTS</span></span>

## <span data-ttu-id="ddd5e-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ddd5e-131">NOTES</span></span>

## <span data-ttu-id="ddd5e-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ddd5e-132">RELATED LINKS</span></span>

[<span data-ttu-id="ddd5e-133">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ddd5e-133">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="ddd5e-134">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="ddd5e-134">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="ddd5e-135">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ddd5e-135">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="ddd5e-136">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ddd5e-136">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)
