---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FF2BFE34-4A12-49F9-9BE5-4084A36BC272
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 609dd0d8732ac83836596ecee9f95cd8d7df3f27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765012"
---
# <span data-ttu-id="faf64-101">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="faf64-101">Set-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="faf64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="faf64-102">SYNOPSIS</span></span>
<span data-ttu-id="faf64-103">Azure depolama tablosu için depolanan erişim ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="faf64-103">Sets the stored access policy for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="faf64-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="faf64-104">SYNTAX</span></span>

```
Set-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="faf64-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="faf64-105">DESCRIPTION</span></span>
<span data-ttu-id="faf64-106">**Set-AzureStorageTableStoredAccessPolicy** cmdlet 'ı bir Azure depolama tablosu için depolanan erişim ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="faf64-106">The **Set-AzureStorageTableStoredAccessPolicy** cmdlet set the stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="faf64-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="faf64-107">EXAMPLES</span></span>

### <span data-ttu-id="faf64-108">Örnek 1: tüm izinle tabloda depolanan bir erişim ilkesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="faf64-108">Example 1: Set a stored access policy in table with full permission</span></span>
```
PS C:\>Set-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy08" -Permission raud
```

<span data-ttu-id="faf64-109">Bu komut, MyTable adlı depolama tablosu için Policy08 adındaki bir erişim ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="faf64-109">This command sets an access policy named Policy08 for storage table named MyTable.</span></span>

## <span data-ttu-id="faf64-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="faf64-110">PARAMETERS</span></span>

### <span data-ttu-id="faf64-111">-Context</span><span class="sxs-lookup"><span data-stu-id="faf64-111">-Context</span></span>
<span data-ttu-id="faf64-112">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="faf64-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="faf64-113">Depolama bağlamı edinmek için New-AzureStorageContext cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="faf64-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="faf64-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="faf64-114">-ExpiryTime</span></span>
<span data-ttu-id="faf64-115">Depolanan erişim ilkesinin zaman dolacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="faf64-115">Specifies the time at which the stored access policy expires.</span></span>

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

### <span data-ttu-id="faf64-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="faf64-116">-NoExpiryTime</span></span>
<span data-ttu-id="faf64-117">Erişim ilkesinde son kullanma tarihi olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="faf64-117">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="faf64-118">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="faf64-118">-NoStartTime</span></span>
<span data-ttu-id="faf64-119">Başlangıç zamanının $Null olarak ayarlandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="faf64-119">Indicates that the start time is set to $Null.</span></span>

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

### <span data-ttu-id="faf64-120">-İzin</span><span class="sxs-lookup"><span data-stu-id="faf64-120">-Permission</span></span>
<span data-ttu-id="faf64-121">Depolanan erişim ilkesinde depolama tablosuna erişim izinlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="faf64-121">Specifies permissions in the stored access policy to access the storage table.</span></span>

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

### <span data-ttu-id="faf64-122">-İlke</span><span class="sxs-lookup"><span data-stu-id="faf64-122">-Policy</span></span>
<span data-ttu-id="faf64-123">Depolanan erişim ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="faf64-123">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="faf64-124">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="faf64-124">-StartTime</span></span>
<span data-ttu-id="faf64-125">Depolanan erişim ilkesinin geçerli olacağı saati belirtir.</span><span class="sxs-lookup"><span data-stu-id="faf64-125">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="faf64-126">-Tablo</span><span class="sxs-lookup"><span data-stu-id="faf64-126">-Table</span></span>
<span data-ttu-id="faf64-127">Azure depolama tablosu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="faf64-127">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="faf64-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="faf64-128">-Confirm</span></span>
<span data-ttu-id="faf64-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="faf64-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="faf64-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="faf64-130">-WhatIf</span></span>
<span data-ttu-id="faf64-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="faf64-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="faf64-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="faf64-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="faf64-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faf64-133">CommonParameters</span></span>
<span data-ttu-id="faf64-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="faf64-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faf64-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="faf64-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faf64-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="faf64-136">INPUTS</span></span>

### <span data-ttu-id="faf64-137">Istoragecontext</span><span class="sxs-lookup"><span data-stu-id="faf64-137">IStorageContext</span></span>

<span data-ttu-id="faf64-138">' Context ' parametresi ardışık düzenin ' ıstoragecontext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="faf64-138">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="faf64-139">Dizisi</span><span class="sxs-lookup"><span data-stu-id="faf64-139">String</span></span>

<span data-ttu-id="faf64-140">Parametre ' tablosu ', ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="faf64-140">Parameter 'Table' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="faf64-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="faf64-141">OUTPUTS</span></span>

### <span data-ttu-id="faf64-142">System. String</span><span class="sxs-lookup"><span data-stu-id="faf64-142">System.String</span></span>

## <span data-ttu-id="faf64-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="faf64-143">NOTES</span></span>

## <span data-ttu-id="faf64-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="faf64-144">RELATED LINKS</span></span>

[<span data-ttu-id="faf64-145">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="faf64-145">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="faf64-146">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="faf64-146">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="faf64-147">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="faf64-147">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="faf64-148">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="faf64-148">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)
