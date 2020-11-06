---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0EB5C25C-D0A1-4444-AEA2-C963D5069CFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 22eac04b24e8fec1778578f4e54792b5dcde6d1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594488"
---
# <span data-ttu-id="af172-101">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="af172-101">Set-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="af172-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af172-102">SYNOPSIS</span></span>
<span data-ttu-id="af172-103">Data Lake Store hesabını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="af172-103">Modifies a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af172-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="af172-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreAccount [-Name] <String> [[-DefaultGroup] <String>] [[-Tag] <Hashtable>]
 [[-TrustedIdProviderState] <TrustedIdProviderState>] [[-FirewallState] <FirewallState>]
 [[-ResourceGroupName] <String>] [-Tier <TierType>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-KeyVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af172-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="af172-105">DESCRIPTION</span></span>
<span data-ttu-id="af172-106">**Set-AzureRmDataLakeStoreAccount** cmdlet 'ı Data Lake Store hesabını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="af172-106">The **Set-AzureRmDataLakeStoreAccount** cmdlet modifies a Data Lake Store account.</span></span>

## <span data-ttu-id="af172-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="af172-107">EXAMPLES</span></span>

### <span data-ttu-id="af172-108">Örnek 1: hesaba etiket ekleme</span><span class="sxs-lookup"><span data-stu-id="af172-108">Example 1: Add a tag to an account</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreAccount -Name "ContosoADL" -Tags @{"stage"="production"}
```

<span data-ttu-id="af172-109">Bu komut, belirtilen etiketi ContosoADL adlı Data Lake Store hesabına ekler.</span><span class="sxs-lookup"><span data-stu-id="af172-109">This command adds the specified tag to the Data Lake Store account named ContosoADL.</span></span>

## <span data-ttu-id="af172-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="af172-110">PARAMETERS</span></span>

### <span data-ttu-id="af172-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="af172-111">-AllowAzureIpState</span></span>
<span data-ttu-id="af172-112">İsteğe bağlı olarak, Azure 'un güvenlik duvarından erişmesine izin ver/engelle.</span><span class="sxs-lookup"><span data-stu-id="af172-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

```yaml
Type: FirewallAllowAzureIpsState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af172-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="af172-113">-DefaultGroup</span></span>
<span data-ttu-id="af172-114">AzureActive Dizin grubunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="af172-114">Specifies the ID of an AzureActive Directory group.</span></span>
<span data-ttu-id="af172-115">Bu grup, oluşturduğunuz dosya ve klasörlerin varsayılan grubudur.</span><span class="sxs-lookup"><span data-stu-id="af172-115">This group is the default group for files and folders that you create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af172-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af172-116">-DefaultProfile</span></span>
<span data-ttu-id="af172-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="af172-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af172-118">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="af172-118">-FirewallState</span></span>
<span data-ttu-id="af172-119">İsteğe bağlı olarak varolan güvenlik duvarı kurallarını etkinleştirme veya devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="af172-119">Optionally enable or disable existing firewall rules.</span></span>

```yaml
Type: FirewallState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af172-120">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="af172-120">-KeyVersion</span></span>
<span data-ttu-id="af172-121">Şifreleme türü Kullanıcı atanmışsa, Kullanıcı anahtar sürümünü Bu parametreyle döndürebilir.</span><span class="sxs-lookup"><span data-stu-id="af172-121">If the encryption type is User assigned, the user can rotate their key version with this parameter.</span></span>

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

### <span data-ttu-id="af172-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="af172-122">-Name</span></span>
<span data-ttu-id="af172-123">Veri Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="af172-123">Specifies the name of a Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af172-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af172-124">-ResourceGroupName</span></span>
<span data-ttu-id="af172-125">Değiştirilecek veri Lake Store hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="af172-125">Specifies the name of the resource group that contains the Data Lake Store account to modify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af172-126">Etiketli</span><span class="sxs-lookup"><span data-stu-id="af172-126">-Tag</span></span>
<span data-ttu-id="af172-127">Etiketleri anahtar-değer çiftleri olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="af172-127">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="af172-128">Diğer Azure kaynaklarından veri Lake Store hesabını belirlemek için Etiketler 'i kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="af172-128">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af172-129">Katmanlı</span><span class="sxs-lookup"><span data-stu-id="af172-129">-Tier</span></span>
<span data-ttu-id="af172-130">Bu hesabın kullanması için istenen taahhüt katmanı.</span><span class="sxs-lookup"><span data-stu-id="af172-130">The desired commitment tier for this account to use.</span></span>

```yaml
Type: TierType
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment1TB, Commitment10TB, Commitment100TB, Commitment500TB, Commitment1PB, Commitment5PB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af172-131">-Trustedivseçproviderstate</span><span class="sxs-lookup"><span data-stu-id="af172-131">-TrustedIdProviderState</span></span>
<span data-ttu-id="af172-132">İsteğe bağlı olarak mevcut güvenilen KIMLIK sağlayıcılarını etkinleştirme veya devre dışı bırakma.</span><span class="sxs-lookup"><span data-stu-id="af172-132">Optionally enable or disable the existing trusted ID providers.</span></span>

```yaml
Type: TrustedIdProviderState
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af172-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af172-133">CommonParameters</span></span>
<span data-ttu-id="af172-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="af172-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af172-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af172-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af172-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="af172-136">INPUTS</span></span>

### <span data-ttu-id="af172-137">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="af172-137">None</span></span>
<span data-ttu-id="af172-138">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="af172-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="af172-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="af172-139">OUTPUTS</span></span>

### <span data-ttu-id="af172-140">PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="af172-140">PSDataLakeStoreAccount</span></span>
<span data-ttu-id="af172-141">Güncelleştirilmiş hesap ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="af172-141">The updated account details.</span></span>

## <span data-ttu-id="af172-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="af172-142">NOTES</span></span>

## <span data-ttu-id="af172-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="af172-143">RELATED LINKS</span></span>

[<span data-ttu-id="af172-144">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="af172-144">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="af172-145">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="af172-145">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="af172-146">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="af172-146">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="af172-147">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="af172-147">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


