---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 58AAA284-45A3-4360-B321-FBE0A3F5D7A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: b05cb9e3789afa905da93642929f65f4965f9b0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765183"
---
# <span data-ttu-id="4d40d-101">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4d40d-101">New-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="4d40d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d40d-102">SYNOPSIS</span></span>
<span data-ttu-id="4d40d-103">Yeni bir Data Lake Store hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4d40d-103">Creates a new Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d40d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4d40d-104">SYNTAX</span></span>

### <span data-ttu-id="4d40d-105">Kullanıcıya veya sisteme atanan şifreleme (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4d40d-105">User or System assigned encryption (Default)</span></span>
```
New-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tags] <Hashtable>] [[-Encryption] <EncryptionConfigType>]
 [[-KeyVaultId] <String>] [[-KeyName] <String>] [[-KeyVersion] <String>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d40d-106">Şifrelemeyi devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="4d40d-106">Disable Encryption</span></span>
```
New-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tags] <Hashtable>] [-DisableEncryption] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d40d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4d40d-107">DESCRIPTION</span></span>
<span data-ttu-id="4d40d-108">**New-AzureRmDataLakeStoreAccount** cmdlet 'i yeni bir Data Lake Store hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4d40d-108">The **New-AzureRmDataLakeStoreAccount** cmdlet creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="4d40d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4d40d-109">EXAMPLES</span></span>

### <span data-ttu-id="4d40d-110">Örnek 1: hesap oluşturma</span><span class="sxs-lookup"><span data-stu-id="4d40d-110">Example 1: Create an account</span></span>
```
PS C:\>New-AzureRmDataLakeStoreAccount -Name "ContosoADL" -ResourceGroupName "ContosoOrg" -Location "East US 2"
```

<span data-ttu-id="4d40d-111">Bu komut, Doğu US 2 konumu için ContosoADL adlı bir Data Lake Store hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4d40d-111">This command creates a Data Lake Store account named ContosoADL for the East US 2 location.</span></span>

## <span data-ttu-id="4d40d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4d40d-112">PARAMETERS</span></span>

### <span data-ttu-id="4d40d-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="4d40d-113">-DefaultGroup</span></span>
<span data-ttu-id="4d40d-114">Yeni dosya ve klasörler için varsayılan Grup sahibi olarak kullanılacak AzureActive Dizin grubunun nesne KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d40d-114">Specifies the object ID of the AzureActive Directory group to use as the default group owner for new files and folders.</span></span>

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

### <span data-ttu-id="4d40d-115">-DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="4d40d-115">-DisableEncryption</span></span>
<span data-ttu-id="4d40d-116">Hesabın, hiçbir şifreleme uygulandığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d40d-116">Indicates that the account will not have any form of encryption applied to it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable Encryption
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d40d-117">-Şifreleme</span><span class="sxs-lookup"><span data-stu-id="4d40d-117">-Encryption</span></span>
```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType]
Parameter Sets: User or System assigned encryption
Aliases: 
Accepted values: UserManaged, ServiceManaged

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d40d-118">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="4d40d-118">-KeyName</span></span>
```yaml
Type: System.String
Parameter Sets: User or System assigned encryption
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d40d-119">-Anahtarlı</span><span class="sxs-lookup"><span data-stu-id="4d40d-119">-KeyVaultId</span></span>
```yaml
Type: System.String
Parameter Sets: User or System assigned encryption
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d40d-120">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="4d40d-120">-KeyVersion</span></span>
```yaml
Type: System.String
Parameter Sets: User or System assigned encryption
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d40d-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="4d40d-121">-Location</span></span>
<span data-ttu-id="4d40d-122">Hesap için kullanılacak konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d40d-122">Specifies the location to use for the account.</span></span>
<span data-ttu-id="4d40d-123">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="4d40d-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4d40d-124">Doğu ABD 2</span><span class="sxs-lookup"><span data-stu-id="4d40d-124">East US 2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d40d-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="4d40d-125">-Name</span></span>
<span data-ttu-id="4d40d-126">Oluşturulacak hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d40d-126">Specifies the name of the account to create.</span></span>

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

### <span data-ttu-id="4d40d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d40d-127">-ResourceGroupName</span></span>
<span data-ttu-id="4d40d-128">Hesabı içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d40d-128">Specifies the name of the resource group that contains the account.</span></span>

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

### <span data-ttu-id="4d40d-129">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="4d40d-129">-Tags</span></span>
<span data-ttu-id="4d40d-130">Etiketleri anahtar-değer çiftleri olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d40d-130">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="4d40d-131">Diğer Azure kaynaklarından veri Lake Store hesabını belirlemek için Etiketler 'i kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4d40d-131">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d40d-132">Katmanlı</span><span class="sxs-lookup"><span data-stu-id="4d40d-132">-Tier</span></span>
<span data-ttu-id="4d40d-133">Bu hesabın kullanması için istenen taahhüt katmanı.</span><span class="sxs-lookup"><span data-stu-id="4d40d-133">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="4d40d-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d40d-134">-DefaultProfile</span></span>
<span data-ttu-id="4d40d-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4d40d-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d40d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d40d-136">CommonParameters</span></span>
<span data-ttu-id="4d40d-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4d40d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d40d-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d40d-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d40d-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4d40d-139">INPUTS</span></span>

## <span data-ttu-id="4d40d-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4d40d-140">OUTPUTS</span></span>

### <span data-ttu-id="4d40d-141">PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4d40d-141">PSDataLakeStoreAccount</span></span>
<span data-ttu-id="4d40d-142">Oluşturulan hesap ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="4d40d-142">The created account details.</span></span>

## <span data-ttu-id="4d40d-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4d40d-143">NOTES</span></span>

## <span data-ttu-id="4d40d-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4d40d-144">RELATED LINKS</span></span>

[<span data-ttu-id="4d40d-145">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4d40d-145">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="4d40d-146">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4d40d-146">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="4d40d-147">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4d40d-147">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="4d40d-148">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="4d40d-148">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


