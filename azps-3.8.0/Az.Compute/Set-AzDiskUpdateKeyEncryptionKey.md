---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskupdatekeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateKeyEncryptionKey.md
ms.openlocfilehash: d37181ae14b0070cd60adca3f6f56f25eab7fd3e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098443"
---
# <span data-ttu-id="d820d-101">Set-AzDiskUpdateKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="d820d-101">Set-AzDiskUpdateKeyEncryptionKey</span></span>

## <span data-ttu-id="d820d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d820d-102">SYNOPSIS</span></span>
<span data-ttu-id="d820d-103">Disk güncelleştirme nesnesinde anahtar şifreleme anahtarı özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d820d-103">Sets the key encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="d820d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d820d-104">SYNTAX</span></span>

```
Set-AzDiskUpdateKeyEncryptionKey [-DiskUpdate] <PSDiskUpdate> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d820d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d820d-105">DESCRIPTION</span></span>
<span data-ttu-id="d820d-106">**Set-AzDiskUpdateKeyEncryptionKey** cmdlet 'i, disk güncelleştirme nesnesinde anahtar şifreleme anahtar özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d820d-106">The **Set-AzDiskUpdateKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="d820d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d820d-107">EXAMPLES</span></span>

### <span data-ttu-id="d820d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d820d-108">Example 1</span></span>
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

<span data-ttu-id="d820d-109">İlk komut Premium_LRS depolama hesabı türünde, boyutu 10 olan yerel bir disk güncelleştirme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d820d-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="d820d-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="d820d-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="d820d-111">İkinci ve üçüncü komut, disk güncelleştirme nesnesi için disk şifrelemesi anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d820d-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="d820d-112">Son komut, disk güncelleştirme nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Disk01 ' adında var olan bir diski güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d820d-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="d820d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d820d-113">PARAMETERS</span></span>

### <span data-ttu-id="d820d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d820d-114">-DefaultProfile</span></span>
<span data-ttu-id="d820d-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d820d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d820d-116">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="d820d-116">-DiskUpdate</span></span>
<span data-ttu-id="d820d-117">Yerel bir disk güncelleştirme nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="d820d-117">Specifies a local disk update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d820d-118">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="d820d-118">-KeyUrl</span></span>
<span data-ttu-id="d820d-119">Anahtar URL 'Sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d820d-119">Specifies the key Url.</span></span>

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

### <span data-ttu-id="d820d-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="d820d-120">-SourceVaultId</span></span>
<span data-ttu-id="d820d-121">Kaynak Kasası KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d820d-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="d820d-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="d820d-122">-Confirm</span></span>
<span data-ttu-id="d820d-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d820d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d820d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d820d-124">-WhatIf</span></span>
<span data-ttu-id="d820d-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d820d-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d820d-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d820d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d820d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d820d-127">CommonParameters</span></span>
<span data-ttu-id="d820d-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d820d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d820d-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d820d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d820d-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d820d-130">INPUTS</span></span>

### <span data-ttu-id="d820d-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDIsReference</span><span class="sxs-lookup"><span data-stu-id="d820d-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

### <span data-ttu-id="d820d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d820d-132">System.String</span></span>

## <span data-ttu-id="d820d-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d820d-133">OUTPUTS</span></span>

### <span data-ttu-id="d820d-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDIsReference</span><span class="sxs-lookup"><span data-stu-id="d820d-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="d820d-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d820d-135">NOTES</span></span>

## <span data-ttu-id="d820d-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d820d-136">RELATED LINKS</span></span>