---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0EB5C25C-D0A1-4444-AEA2-C963D5069CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreAccount.md
ms.openlocfilehash: 0754bd515a846f8524bc7fd9826d36d19d79843a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752285"
---
# <span data-ttu-id="79ed8-101">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="79ed8-101">Set-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="79ed8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79ed8-102">SYNOPSIS</span></span>
<span data-ttu-id="79ed8-103">Data Lake Store hesabını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="79ed8-103">Modifies a Data Lake Store account.</span></span>

## <span data-ttu-id="79ed8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="79ed8-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreAccount [-Name] <String> [[-DefaultGroup] <String>] [[-Tag] <Hashtable>]
 [[-TrustedIdProviderState] <TrustedIdProviderState>] [[-FirewallState] <FirewallState>]
 [[-ResourceGroupName] <String>] [-Tier <TierType>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-KeyVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79ed8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="79ed8-105">DESCRIPTION</span></span>
<span data-ttu-id="79ed8-106">**Set-AzDataLakeStoreAccount** cmdlet 'ı Data Lake Store hesabını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="79ed8-106">The **Set-AzDataLakeStoreAccount** cmdlet modifies a Data Lake Store account.</span></span>

## <span data-ttu-id="79ed8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="79ed8-107">EXAMPLES</span></span>

### <span data-ttu-id="79ed8-108">Örnek 1: hesaba etiket ekleme</span><span class="sxs-lookup"><span data-stu-id="79ed8-108">Example 1: Add a tag to an account</span></span>
```
PS C:\>Set-AzDataLakeStoreAccount -Name "ContosoADL" -Tags @{"stage"="production"}
```

<span data-ttu-id="79ed8-109">Bu komut, belirtilen etiketi ContosoADL adlı Data Lake Store hesabına ekler.</span><span class="sxs-lookup"><span data-stu-id="79ed8-109">This command adds the specified tag to the Data Lake Store account named ContosoADL.</span></span>

## <span data-ttu-id="79ed8-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="79ed8-110">PARAMETERS</span></span>

### <span data-ttu-id="79ed8-111">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="79ed8-111">-AllowAzureIpState</span></span>
<span data-ttu-id="79ed8-112">İsteğe bağlı olarak, Azure 'un güvenlik duvarından erişmesine izin ver/engelle.</span><span class="sxs-lookup"><span data-stu-id="79ed8-112">Optionally allow/block Azure originating IPs through the firewall.</span></span>

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

### <span data-ttu-id="79ed8-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="79ed8-113">-DefaultGroup</span></span>
<span data-ttu-id="79ed8-114">AzureActive Dizin grubunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="79ed8-114">Specifies the ID of an AzureActive Directory group.</span></span>
<span data-ttu-id="79ed8-115">Bu grup, oluşturduğunuz dosya ve klasörlerin varsayılan grubudur.</span><span class="sxs-lookup"><span data-stu-id="79ed8-115">This group is the default group for files and folders that you create.</span></span>

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

### <span data-ttu-id="79ed8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79ed8-116">-DefaultProfile</span></span>
<span data-ttu-id="79ed8-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="79ed8-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79ed8-118">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="79ed8-118">-FirewallState</span></span>
<span data-ttu-id="79ed8-119">İsteğe bağlı olarak varolan güvenlik duvarı kurallarını etkinleştirme veya devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="79ed8-119">Optionally enable or disable existing firewall rules.</span></span>

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

### <span data-ttu-id="79ed8-120">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="79ed8-120">-KeyVersion</span></span>
<span data-ttu-id="79ed8-121">Şifreleme türü Kullanıcı atanmışsa, Kullanıcı anahtar sürümünü Bu parametreyle döndürebilir.</span><span class="sxs-lookup"><span data-stu-id="79ed8-121">If the encryption type is User assigned, the user can rotate their key version with this parameter.</span></span>

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

### <span data-ttu-id="79ed8-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="79ed8-122">-Name</span></span>
<span data-ttu-id="79ed8-123">Veri Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79ed8-123">Specifies the name of a Data Lake Store account.</span></span>

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

### <span data-ttu-id="79ed8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79ed8-124">-ResourceGroupName</span></span>
<span data-ttu-id="79ed8-125">Değiştirilecek veri Lake Store hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79ed8-125">Specifies the name of the resource group that contains the Data Lake Store account to modify.</span></span>

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

### <span data-ttu-id="79ed8-126">Etiketli</span><span class="sxs-lookup"><span data-stu-id="79ed8-126">-Tag</span></span>
<span data-ttu-id="79ed8-127">Etiketleri anahtar-değer çiftleri olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="79ed8-127">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="79ed8-128">Diğer Azure kaynaklarından veri Lake Store hesabını belirlemek için Etiketler 'i kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="79ed8-128">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

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

### <span data-ttu-id="79ed8-129">Katmanlı</span><span class="sxs-lookup"><span data-stu-id="79ed8-129">-Tier</span></span>
<span data-ttu-id="79ed8-130">Bu hesabın kullanması için istenen taahhüt katmanı.</span><span class="sxs-lookup"><span data-stu-id="79ed8-130">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="79ed8-131">-Trustedivseçproviderstate</span><span class="sxs-lookup"><span data-stu-id="79ed8-131">-TrustedIdProviderState</span></span>
<span data-ttu-id="79ed8-132">İsteğe bağlı olarak mevcut güvenilen KIMLIK sağlayıcılarını etkinleştirme veya devre dışı bırakma.</span><span class="sxs-lookup"><span data-stu-id="79ed8-132">Optionally enable or disable the existing trusted ID providers.</span></span>

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

### <span data-ttu-id="79ed8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79ed8-133">CommonParameters</span></span>
<span data-ttu-id="79ed8-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="79ed8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79ed8-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79ed8-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79ed8-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="79ed8-136">INPUTS</span></span>

### <span data-ttu-id="79ed8-137">System. String</span><span class="sxs-lookup"><span data-stu-id="79ed8-137">System.String</span></span>

### <span data-ttu-id="79ed8-138">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="79ed8-138">System.Collections.Hashtable</span></span>

### <span data-ttu-id="79ed8-139">System. Nullable ' 1 [[Microsoft. Azure. Management. DataLake. Store. modeller. Trustedivseçproviderstate, Microsoft. Azure. Management. DataLake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="79ed8-139">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TrustedIdProviderState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="79ed8-140">System. Nullable ' 1 [[Microsoft. Azure. Management. DataLake. Store. modeller. FirewallState, Microsoft. Azure. Management. DataLake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="79ed8-140">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.FirewallState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="79ed8-141">System. Nullable ' 1 [[Microsoft. Azure. Management. DataLake. Store. modeller. TierType, Microsoft. Azure. Management. DataLake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="79ed8-141">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="79ed8-142">System. Nullable ' 1 [[Microsoft. Azure. Management. DataLake. Store. modeller. FirewallAllowAzureIpsState, Microsoft. Azure. Management. DataLake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="79ed8-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.FirewallAllowAzureIpsState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="79ed8-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="79ed8-143">OUTPUTS</span></span>

### <span data-ttu-id="79ed8-144">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="79ed8-144">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="79ed8-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="79ed8-145">NOTES</span></span>

## <span data-ttu-id="79ed8-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="79ed8-146">RELATED LINKS</span></span>

[<span data-ttu-id="79ed8-147">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="79ed8-147">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="79ed8-148">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="79ed8-148">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="79ed8-149">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="79ed8-149">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="79ed8-150">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="79ed8-150">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)

