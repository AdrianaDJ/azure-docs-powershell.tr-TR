---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskupdatekeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateKeyEncryptionKey.md
ms.openlocfilehash: 5a6ea0eede8c7e9f6311c5d951f8e19176f532c6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752725"
---
# <span data-ttu-id="ee3f3-101">Set-AzDiskUpdateKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="ee3f3-101">Set-AzDiskUpdateKeyEncryptionKey</span></span>

## <span data-ttu-id="ee3f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee3f3-102">SYNOPSIS</span></span>
<span data-ttu-id="ee3f3-103">Disk güncelleştirme nesnesinde anahtar şifreleme anahtarı özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ee3f3-103">Sets the key encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="ee3f3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ee3f3-104">SYNTAX</span></span>

```
Set-AzDiskUpdateKeyEncryptionKey [-DiskUpdate] <PSDiskUpdate> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee3f3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ee3f3-105">DESCRIPTION</span></span>
<span data-ttu-id="ee3f3-106">**Set-AzDiskUpdateKeyEncryptionKey** cmdlet 'i, disk güncelleştirme nesnesinde anahtar şifreleme anahtar özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ee3f3-106">The **Set-AzDiskUpdateKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="ee3f3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ee3f3-107">EXAMPLES</span></span>

### <span data-ttu-id="ee3f3-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ee3f3-108">Example 1</span></span>
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

<span data-ttu-id="ee3f3-109">İlk komut Premium_LRS depolama hesabı türünde, boyutu 10 olan yerel bir disk güncelleştirme nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ee3f3-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="ee3f3-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="ee3f3-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="ee3f3-111">İkinci ve üçüncü komut, disk güncelleştirme nesnesi için disk şifrelemesi anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ee3f3-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="ee3f3-112">Son komut, disk güncelleştirme nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Disk01 ' adında var olan bir diski güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ee3f3-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="ee3f3-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ee3f3-113">PARAMETERS</span></span>

### <span data-ttu-id="ee3f3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee3f3-114">-DefaultProfile</span></span>
<span data-ttu-id="ee3f3-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ee3f3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee3f3-116">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="ee3f3-116">-DiskUpdate</span></span>
<span data-ttu-id="ee3f3-117">Yerel bir disk güncelleştirme nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee3f3-117">Specifies a local disk update object.</span></span>

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

### <span data-ttu-id="ee3f3-118">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="ee3f3-118">-KeyUrl</span></span>
<span data-ttu-id="ee3f3-119">Anahtar URL 'Sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee3f3-119">Specifies the key Url.</span></span>

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

### <span data-ttu-id="ee3f3-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="ee3f3-120">-SourceVaultId</span></span>
<span data-ttu-id="ee3f3-121">Kaynak Kasası KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee3f3-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="ee3f3-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="ee3f3-122">-Confirm</span></span>
<span data-ttu-id="ee3f3-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ee3f3-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee3f3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee3f3-124">-WhatIf</span></span>
<span data-ttu-id="ee3f3-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ee3f3-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ee3f3-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ee3f3-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee3f3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee3f3-127">CommonParameters</span></span>
<span data-ttu-id="ee3f3-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ee3f3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee3f3-129">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ee3f3-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee3f3-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ee3f3-130">INPUTS</span></span>

### <span data-ttu-id="ee3f3-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDIsReference</span><span class="sxs-lookup"><span data-stu-id="ee3f3-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

### <span data-ttu-id="ee3f3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ee3f3-132">System.String</span></span>

## <span data-ttu-id="ee3f3-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ee3f3-133">OUTPUTS</span></span>

### <span data-ttu-id="ee3f3-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDIsReference</span><span class="sxs-lookup"><span data-stu-id="ee3f3-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="ee3f3-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ee3f3-135">NOTES</span></span>

## <span data-ttu-id="ee3f3-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ee3f3-136">RELATED LINKS</span></span>
