---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskkeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskKeyEncryptionKey.md
ms.openlocfilehash: c207ccf33b42cf0e7cf1fdb319d0ba17d040d3d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752731"
---
# <span data-ttu-id="a51cd-101">Set-AzDiskKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="a51cd-101">Set-AzDiskKeyEncryptionKey</span></span>

## <span data-ttu-id="a51cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a51cd-102">SYNOPSIS</span></span>
<span data-ttu-id="a51cd-103">Disk nesnesinde anahtar şifreleme anahtarı özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a51cd-103">Sets the key encryption key properties on a disk object.</span></span>

## <span data-ttu-id="a51cd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a51cd-104">SYNTAX</span></span>

```
Set-AzDiskKeyEncryptionKey [-Disk] <PSDisk> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a51cd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a51cd-105">DESCRIPTION</span></span>
<span data-ttu-id="a51cd-106">**Set-AzDiskKeyEncryptionKey** cmdlet 'i, disk nesnesinde anahtar şifreleme anahtar özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a51cd-106">The **Set-AzDiskKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk object.</span></span>

## <span data-ttu-id="a51cd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a51cd-107">EXAMPLES</span></span>

### <span data-ttu-id="a51cd-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a51cd-108">Example 1</span></span>
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

<span data-ttu-id="a51cd-109">İlk komut Standard_LRS depolama hesabı türünde, 5 GB boyutundaki yerel bir boş disk nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a51cd-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="a51cd-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="a51cd-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="a51cd-111">İkinci ve üçüncü komut, disk nesnesinin disk şifrelemesi anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a51cd-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="a51cd-112">Son komut, disk nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Disk01 ' adında bir disk oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a51cd-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="a51cd-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a51cd-113">PARAMETERS</span></span>

### <span data-ttu-id="a51cd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a51cd-114">-DefaultProfile</span></span>
<span data-ttu-id="a51cd-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a51cd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a51cd-116">-Disk</span><span class="sxs-lookup"><span data-stu-id="a51cd-116">-Disk</span></span>
<span data-ttu-id="a51cd-117">Yerel bir disk nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a51cd-117">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a51cd-118">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="a51cd-118">-KeyUrl</span></span>
<span data-ttu-id="a51cd-119">Anahtar URL 'Sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a51cd-119">Specifies the key Url.</span></span>

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

### <span data-ttu-id="a51cd-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="a51cd-120">-SourceVaultId</span></span>
<span data-ttu-id="a51cd-121">Kaynak Kasası KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a51cd-121">Specifies the source vault ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a51cd-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="a51cd-122">-Confirm</span></span>
<span data-ttu-id="a51cd-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a51cd-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a51cd-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a51cd-124">-WhatIf</span></span>
<span data-ttu-id="a51cd-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a51cd-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a51cd-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a51cd-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a51cd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a51cd-127">CommonParameters</span></span>
<span data-ttu-id="a51cd-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a51cd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a51cd-129">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a51cd-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a51cd-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a51cd-130">INPUTS</span></span>

### <span data-ttu-id="a51cd-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDİsk</span><span class="sxs-lookup"><span data-stu-id="a51cd-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="a51cd-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a51cd-132">System.String</span></span>

## <span data-ttu-id="a51cd-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a51cd-133">OUTPUTS</span></span>

### <span data-ttu-id="a51cd-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDİsk</span><span class="sxs-lookup"><span data-stu-id="a51cd-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="a51cd-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a51cd-135">NOTES</span></span>

## <span data-ttu-id="a51cd-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a51cd-136">RELATED LINKS</span></span>
