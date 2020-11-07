---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzDisk.md
ms.openlocfilehash: 1eea8504f974e7ffc504520a5b5abc036c4d3e2a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936977"
---
# <span data-ttu-id="d3645-101">New-AzDisk</span><span class="sxs-lookup"><span data-stu-id="d3645-101">New-AzDisk</span></span>

## <span data-ttu-id="d3645-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3645-102">SYNOPSIS</span></span>
<span data-ttu-id="d3645-103">Yönetilen bir disk oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d3645-103">Creates a managed disk.</span></span>

## <span data-ttu-id="d3645-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d3645-104">SYNTAX</span></span>

```
New-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3645-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d3645-105">DESCRIPTION</span></span>
<span data-ttu-id="d3645-106">**Yeni-azdisk** cmdlet 'i yönetilen bir disk oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d3645-106">The **New-AzDisk** cmdlet creates a managed disk.</span></span>

## <span data-ttu-id="d3645-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d3645-107">EXAMPLES</span></span>

### <span data-ttu-id="d3645-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d3645-108">Example 1</span></span>
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

<span data-ttu-id="d3645-109">İlk komut Standard_LRS depolama hesabı türünde, 5 GB boyutundaki yerel bir boş disk nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d3645-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="d3645-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="d3645-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="d3645-111">İkinci ve üçüncü komut, disk nesnesinin disk şifrelemesi anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d3645-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="d3645-112">Son komut, disk nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Disk01 ' adında bir disk oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d3645-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="d3645-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d3645-113">PARAMETERS</span></span>

### <span data-ttu-id="d3645-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="d3645-114">-AsJob</span></span>
<span data-ttu-id="d3645-115">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="d3645-115">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3645-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3645-116">-DefaultProfile</span></span>
<span data-ttu-id="d3645-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d3645-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3645-118">-Disk</span><span class="sxs-lookup"><span data-stu-id="d3645-118">-Disk</span></span>
<span data-ttu-id="d3645-119">Yerel bir disk nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3645-119">Specifies a local disk object.</span></span>

```yaml
Type: PSDisk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3645-120">-DiskName</span><span class="sxs-lookup"><span data-stu-id="d3645-120">-DiskName</span></span>
<span data-ttu-id="d3645-121">Diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3645-121">Specifies the name of a disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3645-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3645-122">-ResourceGroupName</span></span>
<span data-ttu-id="d3645-123">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3645-123">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3645-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="d3645-124">-Confirm</span></span>
<span data-ttu-id="d3645-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d3645-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3645-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3645-126">-WhatIf</span></span>
<span data-ttu-id="d3645-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d3645-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3645-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d3645-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3645-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3645-129">CommonParameters</span></span>
<span data-ttu-id="d3645-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d3645-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3645-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3645-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3645-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d3645-132">INPUTS</span></span>

### <span data-ttu-id="d3645-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d3645-133">System.String</span></span>
<span data-ttu-id="d3645-134">Microsoft. Azure. Management. COMPUTE. modeller. disk</span><span class="sxs-lookup"><span data-stu-id="d3645-134">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="d3645-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d3645-135">OUTPUTS</span></span>

### <span data-ttu-id="d3645-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSDİsk</span><span class="sxs-lookup"><span data-stu-id="d3645-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="d3645-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d3645-137">NOTES</span></span>

## <span data-ttu-id="d3645-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d3645-138">RELATED LINKS</span></span>

