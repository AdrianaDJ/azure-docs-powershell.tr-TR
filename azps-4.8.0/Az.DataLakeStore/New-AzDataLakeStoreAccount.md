---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 58AAA284-45A3-4360-B321-FBE0A3F5D7A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/new-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreAccount.md
ms.openlocfilehash: 4bdf13b485486a8e3c40023ea0011d12b21a93b8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267793"
---
# <span data-ttu-id="450f3-101">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="450f3-101">New-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="450f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="450f3-102">SYNOPSIS</span></span>
<span data-ttu-id="450f3-103">Yeni bir Data Lake Store hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="450f3-103">Creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="450f3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="450f3-104">SYNTAX</span></span>

### <span data-ttu-id="450f3-105">UserOrSystemAssignedEncryption (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="450f3-105">UserOrSystemAssignedEncryption (Default)</span></span>
```
New-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [[-Encryption] <EncryptionConfigType>]
 [[-KeyVaultId] <String>] [[-KeyName] <String>] [[-KeyVersion] <String>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="450f3-106">DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="450f3-106">DisableEncryption</span></span>
```
New-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [-DisableEncryption] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="450f3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="450f3-107">DESCRIPTION</span></span>
<span data-ttu-id="450f3-108">**New-AzDataLakeStoreAccount** cmdlet 'i yeni bir Data Lake Store hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="450f3-108">The **New-AzDataLakeStoreAccount** cmdlet creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="450f3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="450f3-109">EXAMPLES</span></span>

### <span data-ttu-id="450f3-110">Örnek 1: hesap oluşturma</span><span class="sxs-lookup"><span data-stu-id="450f3-110">Example 1: Create an account</span></span>
```
PS C:\>New-AzDataLakeStoreAccount -Name "ContosoADL" -ResourceGroupName "ContosoOrg" -Location "East US 2"
```

<span data-ttu-id="450f3-111">Bu komut, Doğu US 2 konumu için ContosoADL adlı bir Data Lake Store hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="450f3-111">This command creates a Data Lake Store account named ContosoADL for the East US 2 location.</span></span>

## <span data-ttu-id="450f3-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="450f3-112">PARAMETERS</span></span>

### <span data-ttu-id="450f3-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="450f3-113">-DefaultGroup</span></span>
<span data-ttu-id="450f3-114">Yeni dosya ve klasörler için varsayılan Grup sahibi olarak kullanılacak AzureActive Dizin grubunun nesne KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="450f3-114">Specifies the object ID of the AzureActive Directory group to use as the default group owner for new files and folders.</span></span>

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

### <span data-ttu-id="450f3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="450f3-115">-DefaultProfile</span></span>
<span data-ttu-id="450f3-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="450f3-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="450f3-117">-DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="450f3-117">-DisableEncryption</span></span>
<span data-ttu-id="450f3-118">Hesabın, hiçbir şifreleme uygulandığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="450f3-118">Indicates that the account will not have any form of encryption applied to it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableEncryption
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="450f3-119">-Şifreleme</span><span class="sxs-lookup"><span data-stu-id="450f3-119">-Encryption</span></span>
```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType]
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:
Accepted values: UserManaged, ServiceManaged

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="450f3-120">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="450f3-120">-KeyName</span></span>
```yaml
Type: System.String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="450f3-121">-Anahtarlı</span><span class="sxs-lookup"><span data-stu-id="450f3-121">-KeyVaultId</span></span>
```yaml
Type: System.String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="450f3-122">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="450f3-122">-KeyVersion</span></span>
```yaml
Type: System.String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="450f3-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="450f3-123">-Location</span></span>
<span data-ttu-id="450f3-124">Hesap için kullanılacak konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="450f3-124">Specifies the location to use for the account.</span></span>
<span data-ttu-id="450f3-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="450f3-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="450f3-126">Doğu ABD 2</span><span class="sxs-lookup"><span data-stu-id="450f3-126">East US 2</span></span>

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

### <span data-ttu-id="450f3-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="450f3-127">-Name</span></span>
<span data-ttu-id="450f3-128">Oluşturulacak hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="450f3-128">Specifies the name of the account to create.</span></span>

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

### <span data-ttu-id="450f3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="450f3-129">-ResourceGroupName</span></span>
<span data-ttu-id="450f3-130">Hesabı içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="450f3-130">Specifies the name of the resource group that contains the account.</span></span>

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

### <span data-ttu-id="450f3-131">Etiketli</span><span class="sxs-lookup"><span data-stu-id="450f3-131">-Tag</span></span>
<span data-ttu-id="450f3-132">Etiketleri anahtar-değer çiftleri olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="450f3-132">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="450f3-133">Diğer Azure kaynaklarından veri Lake Store hesabını belirlemek için Etiketler 'i kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="450f3-133">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

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

### <span data-ttu-id="450f3-134">Katmanlı</span><span class="sxs-lookup"><span data-stu-id="450f3-134">-Tier</span></span>
<span data-ttu-id="450f3-135">Bu hesabın kullanması için istenen taahhüt katmanı.</span><span class="sxs-lookup"><span data-stu-id="450f3-135">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="450f3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="450f3-136">CommonParameters</span></span>
<span data-ttu-id="450f3-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="450f3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="450f3-138">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="450f3-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="450f3-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="450f3-139">INPUTS</span></span>

### <span data-ttu-id="450f3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="450f3-140">System.String</span></span>

### <span data-ttu-id="450f3-141">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="450f3-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="450f3-142">System. Nullable ' 1 [[Microsoft. Azure. Management. DataLake. Store. modeller. EncryptionConfigType, Microsoft. Azure. Management. DataLake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="450f3-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="450f3-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="450f3-143">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="450f3-144">System. Nullable ' 1 [[Microsoft. Azure. Management. DataLake. Store. modeller. TierType, Microsoft. Azure. Management. DataLake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="450f3-144">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="450f3-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="450f3-145">OUTPUTS</span></span>

### <span data-ttu-id="450f3-146">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="450f3-146">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="450f3-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="450f3-147">NOTES</span></span>

## <span data-ttu-id="450f3-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="450f3-148">RELATED LINKS</span></span>

[<span data-ttu-id="450f3-149">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="450f3-149">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="450f3-150">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="450f3-150">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="450f3-151">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="450f3-151">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="450f3-152">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="450f3-152">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


