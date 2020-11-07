---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskDiskEncryptionKey.md
ms.openlocfilehash: ebba477d319de3bca6a8aac5fda469ded4dbe6d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762276"
---
# <span data-ttu-id="24c3c-101">Set-AzureRmDiskDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="24c3c-101">Set-AzureRmDiskDiskEncryptionKey</span></span>

## <span data-ttu-id="24c3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24c3c-102">SYNOPSIS</span></span>
<span data-ttu-id="24c3c-103">Disk nesnesinin disk şifrelemesi anahtar özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="24c3c-103">Sets the disk encryption key properties on a disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24c3c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="24c3c-104">SYNTAX</span></span>

```
Set-AzureRmDiskDiskEncryptionKey [-Disk] <PSDisk> [[-SecretUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24c3c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="24c3c-105">DESCRIPTION</span></span>
<span data-ttu-id="24c3c-106">**Set-AzureRmDiskDiskEncryptionKey** cmdlet 'i, disk nesnesinin disk şifrelemesi anahtar özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="24c3c-106">The **Set-AzureRmDiskDiskEncryptionKey** cmdlet sets the disk encryption key properties on a disk object.</span></span>

## <span data-ttu-id="24c3c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="24c3c-107">EXAMPLES</span></span>

### <span data-ttu-id="24c3c-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="24c3c-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzureRmDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzureRmDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="24c3c-109">İlk komut Standard_LRS depolama hesabı türünde, 5 GB boyutundaki yerel bir boş disk nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="24c3c-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="24c3c-110">Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.</span><span class="sxs-lookup"><span data-stu-id="24c3c-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="24c3c-111">İkinci ve üçüncü komut, disk nesnesinin disk şifrelemesi anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="24c3c-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="24c3c-112">Son komut, disk nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Disk01 ' adında bir disk oluşturur.</span><span class="sxs-lookup"><span data-stu-id="24c3c-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="24c3c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="24c3c-113">PARAMETERS</span></span>

### <span data-ttu-id="24c3c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24c3c-114">-DefaultProfile</span></span>
<span data-ttu-id="24c3c-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="24c3c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24c3c-116">-Disk</span><span class="sxs-lookup"><span data-stu-id="24c3c-116">-Disk</span></span>
<span data-ttu-id="24c3c-117">Yerel bir disk nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="24c3c-117">Specifies a local disk object.</span></span>

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

### <span data-ttu-id="24c3c-118">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="24c3c-118">-SecretUrl</span></span>
<span data-ttu-id="24c3c-119">Gizli URL 'Yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="24c3c-119">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="24c3c-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="24c3c-120">-SourceVaultId</span></span>
<span data-ttu-id="24c3c-121">Kaynak Kasası KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="24c3c-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="24c3c-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="24c3c-122">-Confirm</span></span>
<span data-ttu-id="24c3c-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="24c3c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24c3c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24c3c-124">-WhatIf</span></span>
<span data-ttu-id="24c3c-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="24c3c-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="24c3c-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="24c3c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24c3c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24c3c-127">CommonParameters</span></span>
<span data-ttu-id="24c3c-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="24c3c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24c3c-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24c3c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24c3c-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="24c3c-130">INPUTS</span></span>

### <span data-ttu-id="24c3c-131">Microsoft. Azure. Management. COMPUTE. modeller. disk</span><span class="sxs-lookup"><span data-stu-id="24c3c-131">Microsoft.Azure.Management.Compute.Models.Disk</span></span>
<span data-ttu-id="24c3c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="24c3c-132">System.String</span></span>

## <span data-ttu-id="24c3c-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="24c3c-133">OUTPUTS</span></span>

### <span data-ttu-id="24c3c-134">Microsoft. Azure. Management. COMPUTE. modeller. disk</span><span class="sxs-lookup"><span data-stu-id="24c3c-134">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="24c3c-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="24c3c-135">NOTES</span></span>

## <span data-ttu-id="24c3c-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="24c3c-136">RELATED LINKS</span></span>

