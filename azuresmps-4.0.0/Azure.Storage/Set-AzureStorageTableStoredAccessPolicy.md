---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: ''
schema: 2.0.0
ms.openlocfilehash: d517ca49f0be3b6add58d151b3b2f79dad17611c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572469"
---
# <span data-ttu-id="d43ab-101">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d43ab-101">Set-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="d43ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d43ab-102">SYNOPSIS</span></span>
<span data-ttu-id="d43ab-103">Azure depolama tablosu için depolanan erişim ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d43ab-103">Sets the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="d43ab-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d43ab-104">SYNTAX</span></span>

```
Set-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d43ab-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d43ab-105">DESCRIPTION</span></span>
<span data-ttu-id="d43ab-106">**Set-AzureStorageTableStoredAccessPolicy** cmdlet 'ı bir Azure depolama tablosu için depolanan erişim ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d43ab-106">The **Set-AzureStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="d43ab-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d43ab-107">EXAMPLES</span></span>

### <span data-ttu-id="d43ab-108">Örnek 1: tüm izinle tabloda depolanan bir erişim ilkesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="d43ab-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08"
```

<span data-ttu-id="d43ab-109">Bu komut, MyTable adlı depolama tablosu için Policy08 adındaki bir erişim ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d43ab-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="d43ab-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d43ab-110">PARAMETERS</span></span>

### <span data-ttu-id="d43ab-111">-Context</span><span class="sxs-lookup"><span data-stu-id="d43ab-111">-Context</span></span>
<span data-ttu-id="d43ab-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d43ab-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d43ab-113">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d43ab-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d43ab-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="d43ab-114">-ExpiryTime</span></span>
<span data-ttu-id="d43ab-115">Depolanan erişim ilkesinin zaman dolacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d43ab-115">Specifies the time at which the stored access policy expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d43ab-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="d43ab-116">-NoExpiryTime</span></span>
<span data-ttu-id="d43ab-117">Erişim ilkesinde son kullanma tarihi olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d43ab-117">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="d43ab-118">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="d43ab-118">-NoStartTime</span></span>
<span data-ttu-id="d43ab-119">Başlangıç zamanının $Null olarak ayarlandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d43ab-119">Indicates that the start time is set to $Null.</span></span>

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

### <span data-ttu-id="d43ab-120">-İzin</span><span class="sxs-lookup"><span data-stu-id="d43ab-120">-Permission</span></span>
<span data-ttu-id="d43ab-121">Bu depolama tablosuna genel erişim düzeyini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d43ab-121">Specifies the level of public access to this storage table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d43ab-122">-İlke</span><span class="sxs-lookup"><span data-stu-id="d43ab-122">-Policy</span></span>
<span data-ttu-id="d43ab-123">Bu SAS belirtecinin izinlerini içeren depolanan bir erişim ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d43ab-123">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d43ab-124">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="d43ab-124">-StartTime</span></span>
<span data-ttu-id="d43ab-125">Depolanan erişim ilkesinin geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="d43ab-125">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d43ab-126">-Tablo</span><span class="sxs-lookup"><span data-stu-id="d43ab-126">-Table</span></span>
<span data-ttu-id="d43ab-127">Azure depolama tablosu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d43ab-127">Specifies the Azure storage table name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d43ab-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="d43ab-128">-Confirm</span></span>
<span data-ttu-id="d43ab-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d43ab-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d43ab-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d43ab-130">-WhatIf</span></span>
<span data-ttu-id="d43ab-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d43ab-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d43ab-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d43ab-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d43ab-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d43ab-133">CommonParameters</span></span>
<span data-ttu-id="d43ab-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d43ab-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d43ab-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d43ab-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d43ab-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d43ab-136">INPUTS</span></span>

## <span data-ttu-id="d43ab-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d43ab-137">OUTPUTS</span></span>

## <span data-ttu-id="d43ab-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d43ab-138">NOTES</span></span>

## <span data-ttu-id="d43ab-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d43ab-139">RELATED LINKS</span></span>

[<span data-ttu-id="d43ab-140">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d43ab-140">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="d43ab-141">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="d43ab-141">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="d43ab-142">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d43ab-142">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="d43ab-143">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d43ab-143">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)
