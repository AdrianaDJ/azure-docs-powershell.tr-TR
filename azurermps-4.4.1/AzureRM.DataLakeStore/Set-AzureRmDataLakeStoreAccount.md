---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0EB5C25C-D0A1-4444-AEA2-C963D5069CFC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: f9ebe1a541baf46e831dbe95b54b2881a03e7454
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763382"
---
# <span data-ttu-id="ae6b1-101">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ae6b1-101">Set-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="ae6b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae6b1-102">SYNOPSIS</span></span>
<span data-ttu-id="ae6b1-103">Data Lake Store hesabını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="ae6b1-103">Modifies a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae6b1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ae6b1-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreAccount [-Name] <String> [[-DefaultGroup] <String>] [[-Tags] <Hashtable>]
 [[-TrustedIdProviderState] <TrustedIdProviderState>] [[-FirewallState] <FirewallState>]
 [[-ResourceGroupName] <String>] [-Tier <TierType>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-KeyVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae6b1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ae6b1-105">DESCRIPTION</span></span>
<span data-ttu-id="ae6b1-106">**Set-AzureRmDataLakeStoreAccount** cmdlet 'ı Data Lake Store hesabını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="ae6b1-106">The **Set-AzureRmDataLakeStoreAccount** cmdlet modifies a Data Lake Store account.</span></span>

## <span data-ttu-id="ae6b1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ae6b1-107">EXAMPLES</span></span>

### <span data-ttu-id="ae6b1-108">Örnek 1: hesaba etiket ekleme</span><span class="sxs-lookup"><span data-stu-id="ae6b1-108">Example 1: Add a tag to an account</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreAccount -Name "ContosoADL" -Tags @{"stage"="production"}
```

<span data-ttu-id="ae6b1-109">Bu komut, belirtilen etiketi ContosoADL adlı Data Lake Store hesabına ekler.</span><span class="sxs-lookup"><span data-stu-id="ae6b1-109">This command adds the specified tag to the Data Lake Store account named ContosoADL.</span></span>

## <span data-ttu-id="ae6b1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ae6b1-110">PARAMETERS</span></span>

### <span data-ttu-id="ae6b1-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="ae6b1-111">-AllowAzureIpState</span></span>
<span data-ttu-id="ae6b1-112">İsteğe bağlı olarak, Azure 'un güvenlik duvarından erişmesine izin ver/engelle.</span><span class="sxs-lookup"><span data-stu-id="ae6b1-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.FirewallAllowAzureIpsState]
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae6b1-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="ae6b1-113">-DefaultGroup</span></span>
<span data-ttu-id="ae6b1-114">AzureActive Dizin grubunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae6b1-114">Specifies the ID of an AzureActive Directory group.</span></span>
<span data-ttu-id="ae6b1-115">Bu grup, oluşturduğunuz dosya ve klasörlerin varsayılan grubudur.</span><span class="sxs-lookup"><span data-stu-id="ae6b1-115">This group is the default group for files and folders that you create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae6b1-116">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="ae6b1-116">-FirewallState</span></span>
<span data-ttu-id="ae6b1-117">İsteğe bağlı olarak varolan güvenlik duvarı kurallarını etkinleştirme veya devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="ae6b1-117">Optionally enable or disable existing firewall rules.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.FirewallState]
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae6b1-118">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="ae6b1-118">-KeyVersion</span></span>
<span data-ttu-id="ae6b1-119">Şifreleme türü Kullanıcı atanmışsa, Kullanıcı anahtar sürümünü Bu parametreyle döndürebilir.</span><span class="sxs-lookup"><span data-stu-id="ae6b1-119">If the encryption type is User assigned, the user can rotate their key version with this parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae6b1-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="ae6b1-120">-Name</span></span>
<span data-ttu-id="ae6b1-121">Veri Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae6b1-121">Specifies the name of a Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae6b1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae6b1-122">-ResourceGroupName</span></span>
<span data-ttu-id="ae6b1-123">Değiştirilecek veri Lake Store hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae6b1-123">Specifies the name of the resource group that contains the Data Lake Store account to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae6b1-124">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="ae6b1-124">-Tags</span></span>
<span data-ttu-id="ae6b1-125">Etiketleri anahtar-değer çiftleri olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae6b1-125">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="ae6b1-126">Diğer Azure kaynaklarından veri Lake Store hesabını belirlemek için Etiketler 'i kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ae6b1-126">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae6b1-127">Katmanlı</span><span class="sxs-lookup"><span data-stu-id="ae6b1-127">-Tier</span></span>
<span data-ttu-id="ae6b1-128">Bu hesabın kullanması için istenen taahhüt katmanı.</span><span class="sxs-lookup"><span data-stu-id="ae6b1-128">The desired commitment tier for this account to use.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TierType]
Parameter Sets: (All)
Aliases: 
Accepted values: Consumption, Commitment1TB, Commitment10TB, Commitment100TB, Commitment500TB, Commitment1PB, Commitment5PB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae6b1-129">-Trustedivseçproviderstate</span><span class="sxs-lookup"><span data-stu-id="ae6b1-129">-TrustedIdProviderState</span></span>
<span data-ttu-id="ae6b1-130">İsteğe bağlı olarak mevcut güvenilen KIMLIK sağlayıcılarını etkinleştirme veya devre dışı bırakma.</span><span class="sxs-lookup"><span data-stu-id="ae6b1-130">Optionally enable or disable the existing trusted ID providers.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TrustedIdProviderState]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae6b1-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae6b1-131">-DefaultProfile</span></span>
<span data-ttu-id="ae6b1-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ae6b1-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae6b1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae6b1-133">CommonParameters</span></span>
<span data-ttu-id="ae6b1-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ae6b1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae6b1-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae6b1-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae6b1-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ae6b1-136">INPUTS</span></span>

## <span data-ttu-id="ae6b1-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ae6b1-137">OUTPUTS</span></span>

### <span data-ttu-id="ae6b1-138">PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ae6b1-138">PSDataLakeStoreAccount</span></span>
<span data-ttu-id="ae6b1-139">Güncelleştirilmiş hesap ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="ae6b1-139">The updated account details.</span></span>

## <span data-ttu-id="ae6b1-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ae6b1-140">NOTES</span></span>

## <span data-ttu-id="ae6b1-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ae6b1-141">RELATED LINKS</span></span>

[<span data-ttu-id="ae6b1-142">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ae6b1-142">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="ae6b1-143">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ae6b1-143">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="ae6b1-144">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ae6b1-144">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="ae6b1-145">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ae6b1-145">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


