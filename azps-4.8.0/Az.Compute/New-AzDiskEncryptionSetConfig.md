---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskencryptionsetconfig.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
ms.openlocfilehash: bfcb306b12c047c9207e0ef2f1d82bf6eaffc4d3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109140"
---
# <span data-ttu-id="c7bd6-101">New-AzDiskEncryptionSetConfig</span><span class="sxs-lookup"><span data-stu-id="c7bd6-101">New-AzDiskEncryptionSetConfig</span></span>

## <span data-ttu-id="c7bd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7bd6-102">SYNOPSIS</span></span>
<span data-ttu-id="c7bd6-103">Yapılandırılabilir bir disk şifrelemesi kümesi nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c7bd6-103">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="c7bd6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c7bd6-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSetConfig [-Location] <String> [[-Tag] <Hashtable>] [[-IdentityType] <String>]
 [[-SourceVaultId] <String>] [-KeyUrl <String>] [-EncryptionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7bd6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c7bd6-105">DESCRIPTION</span></span>
<span data-ttu-id="c7bd6-106">Yapılandırılabilir bir disk şifrelemesi kümesi nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c7bd6-106">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="c7bd6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c7bd6-107">EXAMPLES</span></span>

### <span data-ttu-id="c7bd6-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c7bd6-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="c7bd6-109">Anahtar kasasındaki verilen etkin anahtarı kullanarak disk şifrelemesi kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c7bd6-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="c7bd6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c7bd6-110">PARAMETERS</span></span>

### <span data-ttu-id="c7bd6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7bd6-111">-DefaultProfile</span></span>
<span data-ttu-id="c7bd6-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c7bd6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7bd6-113">-Şifrelemetürü</span><span class="sxs-lookup"><span data-stu-id="c7bd6-113">-EncryptionType</span></span>
<span data-ttu-id="c7bd6-114">Disk şifrelemesi kümesinin şifreleme türünü ayarlamak için bunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="c7bd6-114">Use this to set the encryption type of the disk encryption set.</span></span> <span data-ttu-id="c7bd6-115">Kullanılabilir değerler: ' EncryptionAtRestWithPlatformKey ', ' EncryptionAtRestWithCustomerKey '.</span><span class="sxs-lookup"><span data-stu-id="c7bd6-115">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7bd6-116">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="c7bd6-116">-IdentityType</span></span>
<span data-ttu-id="c7bd6-117">DiskEncryptionSet tarafından kullanılan yönetilen kimliğin türü.</span><span class="sxs-lookup"><span data-stu-id="c7bd6-117">The type of Managed Identity used by the DiskEncryptionSet.</span></span> <span data-ttu-id="c7bd6-118">Yalnızca SystemAssigned destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="c7bd6-118">Only SystemAssigned is supported.</span></span>

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

### <span data-ttu-id="c7bd6-119">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="c7bd6-119">-KeyUrl</span></span>
<span data-ttu-id="c7bd6-120">Tuş Kasası 'ndaki etkin anahtarı gösteren URL</span><span class="sxs-lookup"><span data-stu-id="c7bd6-120">Url pointing to the active key in KeyVault</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7bd6-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="c7bd6-121">-Location</span></span>
<span data-ttu-id="c7bd6-122">Bir konum belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7bd6-122">Specifies a location.</span></span>

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

### <span data-ttu-id="c7bd6-123">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="c7bd6-123">-SourceVaultId</span></span>
<span data-ttu-id="c7bd6-124">Etkin anahtarı içeren tuş Kasası kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="c7bd6-124">Resource id of the KeyVault containing the active key.</span></span>

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

### <span data-ttu-id="c7bd6-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="c7bd6-125">-Tag</span></span>
<span data-ttu-id="c7bd6-126">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="c7bd6-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c7bd6-127">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="c7bd6-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7bd6-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="c7bd6-128">-Confirm</span></span>
<span data-ttu-id="c7bd6-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c7bd6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7bd6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7bd6-130">-WhatIf</span></span>
<span data-ttu-id="c7bd6-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c7bd6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7bd6-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c7bd6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7bd6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7bd6-133">CommonParameters</span></span>
<span data-ttu-id="c7bd6-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c7bd6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7bd6-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c7bd6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7bd6-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c7bd6-136">INPUTS</span></span>

### <span data-ttu-id="c7bd6-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c7bd6-137">System.String</span></span>

### <span data-ttu-id="c7bd6-138">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c7bd6-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c7bd6-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c7bd6-139">OUTPUTS</span></span>

### <span data-ttu-id="c7bd6-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSDıskencryptionset</span><span class="sxs-lookup"><span data-stu-id="c7bd6-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="c7bd6-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c7bd6-141">NOTES</span></span>

## <span data-ttu-id="c7bd6-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c7bd6-142">RELATED LINKS</span></span>
