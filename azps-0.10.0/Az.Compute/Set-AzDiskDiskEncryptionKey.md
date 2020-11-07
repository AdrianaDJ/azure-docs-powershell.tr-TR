---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzDiskDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzDiskDiskEncryptionKey.md
ms.openlocfilehash: 1b0f223514e8d1f740c9341d29f78a4a5d08108d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936877"
---
# <span data-ttu-id="556cd-101">Set-AzDiskDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="556cd-101">Set-AzDiskDiskEncryptionKey</span></span>

## <span data-ttu-id="556cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="556cd-102">SYNOPSIS</span></span>
<span data-ttu-id="556cd-103">Disk nesnesinin disk şifrelemesi anahtar özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="556cd-103">Sets the disk encryption key properties on a disk object.</span></span>

## <span data-ttu-id="556cd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="556cd-104">SYNTAX</span></span>

```
Set-AzDiskDiskEncryptionKey [-Disk] <PSDisk> [[-SecretUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="556cd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="556cd-105">DESCRIPTION</span></span>
<span data-ttu-id="556cd-106">**Set-AzDiskDiskEncryptionKey** cmdlet 'i, disk nesnesinin disk şifrelemesi anahtar özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="556cd-106">The **Set-AzDiskDiskEncryptionKey** cmdlet sets the disk encryption key properties on a disk object.</span></span>

## <span data-ttu-id="556cd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="556cd-107">EXAMPLES</span></span>

### <span data-ttu-id="556cd-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="556cd-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="556cd-109">İlk komut Standard_LRS depolama hesabı türünde, 5 GB boyutundaki yerel bir boş disk nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="556cd-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="556cd-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="556cd-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="556cd-111">İkinci ve üçüncü komut, disk nesnesinin disk şifrelemesi anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="556cd-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="556cd-112">Son komut, disk nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Disk01 ' adında bir disk oluşturur.</span><span class="sxs-lookup"><span data-stu-id="556cd-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="556cd-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="556cd-113">PARAMETERS</span></span>

### <span data-ttu-id="556cd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="556cd-114">-DefaultProfile</span></span>
<span data-ttu-id="556cd-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="556cd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="556cd-116">-Disk</span><span class="sxs-lookup"><span data-stu-id="556cd-116">-Disk</span></span>
<span data-ttu-id="556cd-117">Yerel bir disk nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="556cd-117">Specifies a local disk object.</span></span>

```yaml
Type: PSDisk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="556cd-118">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="556cd-118">-SecretUrl</span></span>
<span data-ttu-id="556cd-119">Gizli URL 'Yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="556cd-119">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="556cd-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="556cd-120">-SourceVaultId</span></span>
<span data-ttu-id="556cd-121">Kaynak Kasası KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="556cd-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="556cd-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="556cd-122">-Confirm</span></span>
<span data-ttu-id="556cd-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="556cd-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="556cd-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="556cd-124">-WhatIf</span></span>
<span data-ttu-id="556cd-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="556cd-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="556cd-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="556cd-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="556cd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="556cd-127">CommonParameters</span></span>
<span data-ttu-id="556cd-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="556cd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="556cd-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="556cd-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="556cd-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="556cd-130">INPUTS</span></span>

### <span data-ttu-id="556cd-131">Microsoft. Azure. Management. COMPUTE. modeller. disk</span><span class="sxs-lookup"><span data-stu-id="556cd-131">Microsoft.Azure.Management.Compute.Models.Disk</span></span>
<span data-ttu-id="556cd-132">System. String</span><span class="sxs-lookup"><span data-stu-id="556cd-132">System.String</span></span>

## <span data-ttu-id="556cd-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="556cd-133">OUTPUTS</span></span>

### <span data-ttu-id="556cd-134">Microsoft. Azure. Management. COMPUTE. modeller. disk</span><span class="sxs-lookup"><span data-stu-id="556cd-134">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="556cd-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="556cd-135">NOTES</span></span>

## <span data-ttu-id="556cd-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="556cd-136">RELATED LINKS</span></span>

