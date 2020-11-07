---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskupdatediskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzDiskUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzDiskUpdateDiskEncryptionKey.md
ms.openlocfilehash: 0f55058bc3419805bf7270e4d03c75db2208669e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936869"
---
# <span data-ttu-id="74d93-101">Set-AzDiskUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="74d93-101">Set-AzDiskUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="74d93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74d93-102">SYNOPSIS</span></span>
<span data-ttu-id="74d93-103">Disk güncelleştirme nesnesinde disk şifrelemesi anahtar özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="74d93-103">Sets the disk encryption key properties on on a disk update object.</span></span>

## <span data-ttu-id="74d93-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="74d93-104">SYNTAX</span></span>

```
Set-AzDiskUpdateDiskEncryptionKey [-DiskUpdate] <PSDiskUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="74d93-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="74d93-105">DESCRIPTION</span></span>
<span data-ttu-id="74d93-106">**Set-AzDiskUpdateDiskEncryptionKey** cmdlet 'i, disk güncelleştirme nesnesinde disk şifrelemesi anahtar özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="74d93-106">The **Set-AzDiskUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on on a disk update object.</span></span>

## <span data-ttu-id="74d93-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="74d93-107">EXAMPLES</span></span>

### <span data-ttu-id="74d93-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="74d93-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="74d93-109">İlk komut Premium_LRS depolama hesabı türünde, boyutu 10 olan yerel bir disk güncelleştirme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="74d93-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="74d93-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="74d93-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="74d93-111">İkinci ve üçüncü komut, disk güncelleştirme nesnesi için disk şifrelemesi anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="74d93-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="74d93-112">Son komut, disk güncelleştirme nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Disk01 ' adında var olan bir diski güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="74d93-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="74d93-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="74d93-113">PARAMETERS</span></span>

### <span data-ttu-id="74d93-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74d93-114">-DefaultProfile</span></span>
<span data-ttu-id="74d93-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="74d93-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74d93-116">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="74d93-116">-DiskUpdate</span></span>
<span data-ttu-id="74d93-117">Yerel bir disk güncelleştirme nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="74d93-117">Specifies a local disk update object.</span></span>

```yaml
Type: PSDiskUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74d93-118">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="74d93-118">-SecretUrl</span></span>
<span data-ttu-id="74d93-119">Gizli URL 'Yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="74d93-119">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="74d93-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="74d93-120">-SourceVaultId</span></span>
<span data-ttu-id="74d93-121">Kaynak Kasası KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="74d93-121">Specifies the source vault ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74d93-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="74d93-122">-Confirm</span></span>
<span data-ttu-id="74d93-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="74d93-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74d93-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74d93-124">-WhatIf</span></span>
<span data-ttu-id="74d93-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="74d93-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74d93-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="74d93-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74d93-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74d93-127">CommonParameters</span></span>
<span data-ttu-id="74d93-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="74d93-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74d93-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74d93-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74d93-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="74d93-130">INPUTS</span></span>

### <span data-ttu-id="74d93-131">Microsoft. Azure. Management. COMPUTE. modeller. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="74d93-131">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>
<span data-ttu-id="74d93-132">System. String</span><span class="sxs-lookup"><span data-stu-id="74d93-132">System.String</span></span>

## <span data-ttu-id="74d93-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="74d93-133">OUTPUTS</span></span>

### <span data-ttu-id="74d93-134">Microsoft. Azure. Management. COMPUTE. modeller. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="74d93-134">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>

## <span data-ttu-id="74d93-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="74d93-135">NOTES</span></span>

## <span data-ttu-id="74d93-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="74d93-136">RELATED LINKS</span></span>

