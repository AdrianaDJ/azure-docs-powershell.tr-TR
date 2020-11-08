---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 931BC75D-B8EF-463D-8FCE-A822093CB05A
online version: ''
schema: 2.0.0
ms.openlocfilehash: bbc1963dbf56d0ef7f31d2174ab352dcc36af619
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106204"
---
# <span data-ttu-id="b4430-101">New-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b4430-101">New-AzureStorageAccount</span></span>

## <span data-ttu-id="b4430-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4430-102">SYNOPSIS</span></span>
<span data-ttu-id="b4430-103">Azure aboneliğindeki yeni bir depolama hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4430-103">Creates a new storage account in an Azure subscription.</span></span>

## <span data-ttu-id="b4430-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b4430-104">SYNTAX</span></span>

### <span data-ttu-id="b4430-105">ParameterSetAffinityGroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b4430-105">ParameterSetAffinityGroup (Default)</span></span>
```
New-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 -AffinityGroup <String> [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b4430-106">ParameterSetLocation</span><span class="sxs-lookup"><span data-stu-id="b4430-106">ParameterSetLocation</span></span>
```
New-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 -Location <String> [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b4430-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b4430-107">DESCRIPTION</span></span>
<span data-ttu-id="b4430-108">**New-AzureStorageAccount** cmdlet 'ı, Azure depolama hizmetleri 'ne erişim sağlayan bir hesap oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4430-108">The **New-AzureStorageAccount** cmdlet creates an account that provides access to Azure storage services.</span></span>
<span data-ttu-id="b4430-109">Depolama hesabı, depolama sistemindeki genel olarak benzersiz bir kaynaktır.</span><span class="sxs-lookup"><span data-stu-id="b4430-109">A storage account is a globally unique resource within the storage system.</span></span>
<span data-ttu-id="b4430-110">Hesap, blob, kuyruk ve tablo hizmetlerinin üst ad alanıdır.</span><span class="sxs-lookup"><span data-stu-id="b4430-110">The account is the parent namespace for the Blob, Queue, and Table services.</span></span>

## <span data-ttu-id="b4430-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b4430-111">EXAMPLES</span></span>

### <span data-ttu-id="b4430-112">Örnek 1: Belirtilen benzeşim grubu için depolama hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="b4430-112">Example 1: Create a storage account for a specified affinity group</span></span>
```
PS C:\> New-AzureStorageAccount -StorageAccountName "azure01" -Label "AzureOne" -AffinityGroup "prodapps"
```

<span data-ttu-id="b4430-113">Bu komut, belirtilen benzeşim grubu için bir depolama hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4430-113">This command creates a storage account for a specified affinity group.</span></span>

### <span data-ttu-id="b4430-114">Örnek 2: belirtilen konumda depolama hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="b4430-114">Example 2: Create a storage account in a specified location</span></span>
```
PS C:\> New-AzureStorageAccount -StorageAccountName "azure02" -Label "AzureTwo" -Location "North Central US"
```

<span data-ttu-id="b4430-115">Bu komut belirtilen konumda depolama hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4430-115">This command creates a storage account in a specified location.</span></span>

## <span data-ttu-id="b4430-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b4430-116">PARAMETERS</span></span>

### <span data-ttu-id="b4430-117">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="b4430-117">-AffinityGroup</span></span>
<span data-ttu-id="b4430-118">Geçerli abonelikte varolan bir benzeşim grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4430-118">Specifies the name of an existing affinity group in the current subscription.</span></span>
<span data-ttu-id="b4430-119">*Location* veya *affinitygroup* parametresini belirtebilirsiniz, ancak ikisini birden belirtemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="b4430-119">You can specify either the *Location* or *AffinityGroup* parameter, but not both.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetAffinityGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4430-120">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="b4430-120">-Description</span></span>
<span data-ttu-id="b4430-121">Depolama hesabı için bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4430-121">Specifies a description for the storage account.</span></span>
<span data-ttu-id="b4430-122">Açıklama en çok 1024 karakter uzunluğunda olabilir.</span><span class="sxs-lookup"><span data-stu-id="b4430-122">The description may be up to 1024 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4430-123">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="b4430-123">-InformationAction</span></span>
<span data-ttu-id="b4430-124">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4430-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b4430-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="b4430-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b4430-126">'A</span><span class="sxs-lookup"><span data-stu-id="b4430-126">Continue</span></span>
- <span data-ttu-id="b4430-127">Manıza</span><span class="sxs-lookup"><span data-stu-id="b4430-127">Ignore</span></span>
- <span data-ttu-id="b4430-128">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="b4430-128">Inquire</span></span>
- <span data-ttu-id="b4430-129">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="b4430-129">SilentlyContinue</span></span>
- <span data-ttu-id="b4430-130">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="b4430-130">Stop</span></span>
- <span data-ttu-id="b4430-131">Biliriz</span><span class="sxs-lookup"><span data-stu-id="b4430-131">Suspend</span></span>

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

### <span data-ttu-id="b4430-132">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="b4430-132">-InformationVariable</span></span>
<span data-ttu-id="b4430-133">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4430-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b4430-134">Etiketli</span><span class="sxs-lookup"><span data-stu-id="b4430-134">-Label</span></span>
<span data-ttu-id="b4430-135">Depolama hesabı için bir etiket belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4430-135">Specifies a label for the storage account.</span></span>
<span data-ttu-id="b4430-136">Etiket en çok 100 karakter uzunluğunda olabilir.</span><span class="sxs-lookup"><span data-stu-id="b4430-136">The label may be up to 100 characters in length.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4430-137">-Konum</span><span class="sxs-lookup"><span data-stu-id="b4430-137">-Location</span></span>
<span data-ttu-id="b4430-138">Depolama hesabının oluşturulduğu Azure veri merkezi konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4430-138">Specifies the Azure data center location where the storage account is created.</span></span>
<span data-ttu-id="b4430-139">*Location* veya *affinitygroup* parametresini içerebilir, ancak ikisini birden içeremez.</span><span class="sxs-lookup"><span data-stu-id="b4430-139">You can include either the *Location* or *AffinityGroup* parameter, but not both.</span></span>

```yaml
Type: String
Parameter Sets: ParameterSetLocation
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4430-140">-Profil</span><span class="sxs-lookup"><span data-stu-id="b4430-140">-Profile</span></span>
<span data-ttu-id="b4430-141">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4430-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b4430-142">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="b4430-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b4430-143">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b4430-143">-StorageAccountName</span></span>
<span data-ttu-id="b4430-144">Depolama hesabı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4430-144">Specifies a name for the storage account.</span></span>
<span data-ttu-id="b4430-145">Depolama hesabı adı Azure için benzersiz olmalıdır ve 3 ila 24 karakter uzunluğunda olmalıdır ve yalnızca küçük harf ve sayılardan oluşmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b4430-145">The storage account name must be unique to Azure and must be between 3 and 24 characters in length and use lowercase letters and numbers only.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4430-146">-Tür</span><span class="sxs-lookup"><span data-stu-id="b4430-146">-Type</span></span>
<span data-ttu-id="b4430-147">Depolama hesabının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4430-147">Specifies the type of the storage account.</span></span>
<span data-ttu-id="b4430-148">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="b4430-148">Valid values are:</span></span>

- <span data-ttu-id="b4430-149">Standard_LRS</span><span class="sxs-lookup"><span data-stu-id="b4430-149">Standard_LRS</span></span>
- <span data-ttu-id="b4430-150">Standard_ZRS</span><span class="sxs-lookup"><span data-stu-id="b4430-150">Standard_ZRS</span></span>
- <span data-ttu-id="b4430-151">Standard_GRS</span><span class="sxs-lookup"><span data-stu-id="b4430-151">Standard_GRS</span></span>
- <span data-ttu-id="b4430-152">Standard_RAGRS</span><span class="sxs-lookup"><span data-stu-id="b4430-152">Standard_RAGRS</span></span>
- <span data-ttu-id="b4430-153">Premium_LRS</span><span class="sxs-lookup"><span data-stu-id="b4430-153">Premium_LRS</span></span>

<span data-ttu-id="b4430-154">Bu parametre belirtilmezse, varsayılan değer Standard_GRS olur.</span><span class="sxs-lookup"><span data-stu-id="b4430-154">If this parameter is not specified, the default value is Standard_GRS.</span></span>

<span data-ttu-id="b4430-155">Standard_ZRS veya Premium_LRS hesapları diğer hesap türleriyle değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="b4430-155">Standard_ZRS or Premium_LRS accounts cannot be changed to other account types, and vice versa.</span></span>

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

### <span data-ttu-id="b4430-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4430-156">CommonParameters</span></span>
<span data-ttu-id="b4430-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b4430-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4430-158">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4430-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4430-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b4430-159">INPUTS</span></span>

## <span data-ttu-id="b4430-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b4430-160">OUTPUTS</span></span>

## <span data-ttu-id="b4430-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b4430-161">NOTES</span></span>

## <span data-ttu-id="b4430-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b4430-162">RELATED LINKS</span></span>

[<span data-ttu-id="b4430-163">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b4430-163">Get-AzureStorageAccount</span></span>](./Get-AzureStorageAccount.md)

[<span data-ttu-id="b4430-164">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b4430-164">Set-AzureStorageAccount</span></span>](./Set-AzureStorageAccount.md)


