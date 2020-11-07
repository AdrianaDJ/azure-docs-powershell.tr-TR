---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotDiskEncryptionKey.md
ms.openlocfilehash: f0c0fa6c8315aef711613dc599027d0653db803e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761248"
---
# <span data-ttu-id="0bed1-101">Set-AzSnapshotDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="0bed1-101">Set-AzSnapshotDiskEncryptionKey</span></span>

## <span data-ttu-id="0bed1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bed1-102">SYNOPSIS</span></span>
<span data-ttu-id="0bed1-103">Anlık görüntü nesnesinde disk şifrelemesi anahtar özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="0bed1-103">Sets the disk encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="0bed1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0bed1-104">SYNTAX</span></span>

```
Set-AzSnapshotDiskEncryptionKey [-Snapshot] <PSSnapshot> [[-SecretUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bed1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0bed1-105">DESCRIPTION</span></span>
<span data-ttu-id="0bed1-106">**Set-AzSnapshotDiskEncryptionKey** cmdlet 'i, anlık görüntü nesnesinde disk şifrelemesi anahtar özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="0bed1-106">The **Set-AzSnapshotDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="0bed1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0bed1-107">EXAMPLES</span></span>

### <span data-ttu-id="0bed1-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0bed1-108">Example 1</span></span>
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

<span data-ttu-id="0bed1-109">İlk komut Standard_LRS depolama hesabı türünde, 5 GB boyutundaki yerel bir boş anlık görüntü nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0bed1-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="0bed1-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="0bed1-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="0bed1-111">İkinci ve üçüncü komutlar, anlık görüntü nesnesinin disk şifreleme anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="0bed1-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="0bed1-112">Son komut, Snapshot nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Snapshot01 ' adıyla bir anlık görüntü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0bed1-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="0bed1-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0bed1-113">PARAMETERS</span></span>

### <span data-ttu-id="0bed1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bed1-114">-DefaultProfile</span></span>
<span data-ttu-id="0bed1-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0bed1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0bed1-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="0bed1-116">-SecretUrl</span></span>
<span data-ttu-id="0bed1-117">Gizli URL 'Yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="0bed1-117">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="0bed1-118">-Anlık görüntü</span><span class="sxs-lookup"><span data-stu-id="0bed1-118">-Snapshot</span></span>
<span data-ttu-id="0bed1-119">Yerel bir anlık görüntü nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="0bed1-119">Specifies a local snapshot object.</span></span>

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

### <span data-ttu-id="0bed1-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="0bed1-120">-SourceVaultId</span></span>
<span data-ttu-id="0bed1-121">Kaynak Kasası KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0bed1-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="0bed1-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="0bed1-122">-Confirm</span></span>
<span data-ttu-id="0bed1-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0bed1-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bed1-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bed1-124">-WhatIf</span></span>
<span data-ttu-id="0bed1-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0bed1-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0bed1-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0bed1-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bed1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bed1-127">CommonParameters</span></span>
<span data-ttu-id="0bed1-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0bed1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bed1-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bed1-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bed1-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0bed1-130">INPUTS</span></span>

### <span data-ttu-id="0bed1-131">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="0bed1-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="0bed1-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0bed1-132">System.String</span></span>

## <span data-ttu-id="0bed1-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0bed1-133">OUTPUTS</span></span>

### <span data-ttu-id="0bed1-134">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="0bed1-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="0bed1-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0bed1-135">NOTES</span></span>

## <span data-ttu-id="0bed1-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0bed1-136">RELATED LINKS</span></span>
