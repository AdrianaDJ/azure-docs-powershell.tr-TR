---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: EB4A7F84-99E4-49B1-856D-EC0736058D23
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8cab29cd7d285d2ae1aae9c007be965e1bbf8f2f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105850"
---
# <span data-ttu-id="7709c-101">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7709c-101">Set-AzureStorageAccount</span></span>

## <span data-ttu-id="7709c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7709c-102">SYNOPSIS</span></span>
<span data-ttu-id="7709c-103">Bir Azure aboneliğindeki depolama hesabının özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7709c-103">Updates the properties of a storage account in an Azure subscription.</span></span>

## <span data-ttu-id="7709c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7709c-104">SYNTAX</span></span>

### <span data-ttu-id="7709c-105">AccountType (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7709c-105">AccountType (Default)</span></span>
```
Set-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7709c-106">GeoReplicationEnabled</span><span class="sxs-lookup"><span data-stu-id="7709c-106">GeoReplicationEnabled</span></span>
```
Set-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 [-GeoReplicationEnabled <Boolean>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7709c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7709c-107">DESCRIPTION</span></span>
<span data-ttu-id="7709c-108">**Set-AzureStorageAccount** cmdlet 'i, geçerli abonelikteki bir Azure depolama hesabının özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7709c-108">The **Set-AzureStorageAccount** cmdlet updates the properties of an Azure storage account in the current subscription.</span></span>
<span data-ttu-id="7709c-109">Ayarlanabilir özellikler şunlardır: **etiket** , **Açıklama** , **tür** ve **GeoReplicationEnabled**.</span><span class="sxs-lookup"><span data-stu-id="7709c-109">Properties that can be set are: **Label** , **Description** , **Type** and **GeoReplicationEnabled**.</span></span>

## <span data-ttu-id="7709c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7709c-110">EXAMPLES</span></span>

### <span data-ttu-id="7709c-111">Örnek 1: depolama hesabının etiketini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="7709c-111">Example 1: Update the label for a storage account</span></span>
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -Label "ContosoAccnt" -Description "Contoso storage account"
```

<span data-ttu-id="7709c-112">Bu komut, ContosoStorage01 adlı depolama hesabının **etiket** ve **Açıklama** özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7709c-112">This command updates the **Label** and **Description** properties for the storage account named ContosoStorage01.</span></span>

### <span data-ttu-id="7709c-113">Örnek 2: depolama hesabı için coğrafi çoğaltma özelliğini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="7709c-113">Example 2: Enable geo-replication for a storage account</span></span>
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -GeoReplicationEnabled $False
```

<span data-ttu-id="7709c-114">Bu komut, ContosoStorage01 adlı depolama hesabı için **GeoReplicationEnabled** özelliğini $false olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7709c-114">This command sets the **GeoReplicationEnabled** property to $False for the storage account named ContosoStorage01.</span></span>

### <span data-ttu-id="7709c-115">Örnek 3: depolama hesabı için Coğrafi çoğaltmayı devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="7709c-115">Example 3: Disable geo-replication for a storage account</span></span>
```
PS C:\> Set-AzureStorageAccount -StorageAccountName "ContosoStorage01" -GeoReplicationEnabled $True
```

<span data-ttu-id="7709c-116">Bu komut, ContosoStorage01 adlı depolama hesabı için **GeoReplicationEnabled** özelliğini $true olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7709c-116">This command sets the **GeoReplicationEnabled** property to $True for the storage account named ContosoStorage01.</span></span>

## <span data-ttu-id="7709c-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7709c-117">PARAMETERS</span></span>

### <span data-ttu-id="7709c-118">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="7709c-118">-Description</span></span>
<span data-ttu-id="7709c-119">Depolama hesabı için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="7709c-119">Specifies a description for the storage account.</span></span>
<span data-ttu-id="7709c-120">Açıklama 1024 karakter uzunluğunda olabilir.</span><span class="sxs-lookup"><span data-stu-id="7709c-120">The description may be up to 1024 characters long.</span></span>

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

### <span data-ttu-id="7709c-121">-GeoReplicationEnabled</span><span class="sxs-lookup"><span data-stu-id="7709c-121">-GeoReplicationEnabled</span></span>
<span data-ttu-id="7709c-122">Depolama hesabının coğrafi çoğaltma 'nın etkin olup olmadığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7709c-122">Specifies whether the storage account is created with the geo-replication enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: GeoReplicationEnabled
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7709c-123">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="7709c-123">-InformationAction</span></span>
<span data-ttu-id="7709c-124">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7709c-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7709c-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7709c-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7709c-126">'A</span><span class="sxs-lookup"><span data-stu-id="7709c-126">Continue</span></span>
- <span data-ttu-id="7709c-127">Manıza</span><span class="sxs-lookup"><span data-stu-id="7709c-127">Ignore</span></span>
- <span data-ttu-id="7709c-128">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="7709c-128">Inquire</span></span>
- <span data-ttu-id="7709c-129">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="7709c-129">SilentlyContinue</span></span>
- <span data-ttu-id="7709c-130">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="7709c-130">Stop</span></span>
- <span data-ttu-id="7709c-131">Biliriz</span><span class="sxs-lookup"><span data-stu-id="7709c-131">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7709c-132">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="7709c-132">-InformationVariable</span></span>
<span data-ttu-id="7709c-133">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="7709c-133">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7709c-134">Etiketli</span><span class="sxs-lookup"><span data-stu-id="7709c-134">-Label</span></span>
<span data-ttu-id="7709c-135">Depolama hesabı için bir etiket belirtir.</span><span class="sxs-lookup"><span data-stu-id="7709c-135">Specifies a label for the storage account.</span></span>
<span data-ttu-id="7709c-136">Etiket en çok 100 karakter uzunluğunda olabilir.</span><span class="sxs-lookup"><span data-stu-id="7709c-136">The label may be up to 100 characters long.</span></span>

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

### <span data-ttu-id="7709c-137">-Profil</span><span class="sxs-lookup"><span data-stu-id="7709c-137">-Profile</span></span>
<span data-ttu-id="7709c-138">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7709c-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7709c-139">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="7709c-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7709c-140">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7709c-140">-StorageAccountName</span></span>
<span data-ttu-id="7709c-141">Bu cmdlet 'in değiştirdiği depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7709c-141">Specifies the name of the storage account that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7709c-142">-Tür</span><span class="sxs-lookup"><span data-stu-id="7709c-142">-Type</span></span>
<span data-ttu-id="7709c-143">Depolama hesabının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="7709c-143">Specifies the type of the storage account.</span></span>
<span data-ttu-id="7709c-144">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="7709c-144">Valid values are:</span></span> 

- <span data-ttu-id="7709c-145">Standard_LRS</span><span class="sxs-lookup"><span data-stu-id="7709c-145">Standard_LRS</span></span>
- <span data-ttu-id="7709c-146">Standard_ZRS</span><span class="sxs-lookup"><span data-stu-id="7709c-146">Standard_ZRS</span></span>
- <span data-ttu-id="7709c-147">Standard_GRS</span><span class="sxs-lookup"><span data-stu-id="7709c-147">Standard_GRS</span></span>
- <span data-ttu-id="7709c-148">Standard_RAGRS</span><span class="sxs-lookup"><span data-stu-id="7709c-148">Standard_RAGRS</span></span>
- <span data-ttu-id="7709c-149">Premium_LRS</span><span class="sxs-lookup"><span data-stu-id="7709c-149">Premium_LRS</span></span>

<span data-ttu-id="7709c-150">Bu parametre belirtilmezse, varsayılan değer Standard_GRS olur.</span><span class="sxs-lookup"><span data-stu-id="7709c-150">If this parameter is not specified, the default value is Standard_GRS.</span></span>

<span data-ttu-id="7709c-151">*GeoReplicationEnabled* parametresini belirtmenin etkisi, *tür* parametresinde Standard_GRS belirtmeyle aynıdır.</span><span class="sxs-lookup"><span data-stu-id="7709c-151">The effect of specifying the *GeoReplicationEnabled* parameter is the same as specifying Standard_GRS in the *Type* parameter.</span></span>

<span data-ttu-id="7709c-152">Standard_ZRS veya Premium_LRS hesapları diğer hesap türleriyle değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="7709c-152">Standard_ZRS or Premium_LRS accounts cannot be changed to other account types, and vice versa.</span></span>

```yaml
Type: String
Parameter Sets: AccountType
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7709c-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7709c-153">CommonParameters</span></span>
<span data-ttu-id="7709c-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7709c-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7709c-155">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7709c-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7709c-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7709c-156">INPUTS</span></span>

## <span data-ttu-id="7709c-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7709c-157">OUTPUTS</span></span>

## <span data-ttu-id="7709c-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7709c-158">NOTES</span></span>

## <span data-ttu-id="7709c-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7709c-159">RELATED LINKS</span></span>

[<span data-ttu-id="7709c-160">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7709c-160">Get-AzureStorageAccount</span></span>](./Get-AzureStorageAccount.md)

[<span data-ttu-id="7709c-161">Yeni-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7709c-161">New-AzureStorageAccount</span></span>](./New-AzureStorageAccount.md)

[<span data-ttu-id="7709c-162">Remove-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7709c-162">Remove-AzureStorageAccount</span></span>](./Remove-AzureStorageAccount.md)


