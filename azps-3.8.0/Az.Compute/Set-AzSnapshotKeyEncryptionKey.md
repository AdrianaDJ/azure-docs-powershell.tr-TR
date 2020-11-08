---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotkeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotKeyEncryptionKey.md
ms.openlocfilehash: c8a3ce4f0e21ac12f73fbcef6a4cb6c3b6b65bad
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096452"
---
# <span data-ttu-id="515b2-101">Set-AzSnapshotKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="515b2-101">Set-AzSnapshotKeyEncryptionKey</span></span>

## <span data-ttu-id="515b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="515b2-102">SYNOPSIS</span></span>
<span data-ttu-id="515b2-103">Anlık görüntü nesnesinde anahtar şifreleme anahtarı özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="515b2-103">Sets the key encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="515b2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="515b2-104">SYNTAX</span></span>

```
Set-AzSnapshotKeyEncryptionKey [-Snapshot] <PSSnapshot> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="515b2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="515b2-105">DESCRIPTION</span></span>
<span data-ttu-id="515b2-106">**Set-AzSnapshotKeyEncryptionKey** cmdlet 'i, anlık görüntü nesnesinde anahtar şifreleme anahtar özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="515b2-106">The **Set-AzSnapshotKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="515b2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="515b2-107">EXAMPLES</span></span>

### <span data-ttu-id="515b2-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="515b2-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="515b2-109">İlk komut Standard_LRS depolama hesabı türünde, 5 GB boyutundaki yerel bir boş anlık görüntü nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="515b2-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="515b2-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="515b2-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="515b2-111">İkinci ve üçüncü komutlar, anlık görüntü nesnesinin disk şifreleme anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="515b2-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="515b2-112">Son komut, Snapshot nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Snapshot01 ' adıyla bir anlık görüntü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="515b2-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="515b2-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="515b2-113">PARAMETERS</span></span>

### <span data-ttu-id="515b2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="515b2-114">-DefaultProfile</span></span>
<span data-ttu-id="515b2-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="515b2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="515b2-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="515b2-116">-KeyUrl</span></span>
<span data-ttu-id="515b2-117">Anahtar URL 'Sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="515b2-117">Specifies the key Url.</span></span>

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

### <span data-ttu-id="515b2-118">-Anlık görüntü</span><span class="sxs-lookup"><span data-stu-id="515b2-118">-Snapshot</span></span>
<span data-ttu-id="515b2-119">Yerel bir anlık görüntü nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="515b2-119">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="515b2-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="515b2-120">-SourceVaultId</span></span>
<span data-ttu-id="515b2-121">Kaynak Kasası KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="515b2-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="515b2-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="515b2-122">-Confirm</span></span>
<span data-ttu-id="515b2-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="515b2-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="515b2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="515b2-124">-WhatIf</span></span>
<span data-ttu-id="515b2-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="515b2-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="515b2-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="515b2-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="515b2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="515b2-127">CommonParameters</span></span>
<span data-ttu-id="515b2-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="515b2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="515b2-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="515b2-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="515b2-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="515b2-130">INPUTS</span></span>

### <span data-ttu-id="515b2-131">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="515b2-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="515b2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="515b2-132">System.String</span></span>

## <span data-ttu-id="515b2-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="515b2-133">OUTPUTS</span></span>

### <span data-ttu-id="515b2-134">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="515b2-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="515b2-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="515b2-135">NOTES</span></span>

## <span data-ttu-id="515b2-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="515b2-136">RELATED LINKS</span></span>
