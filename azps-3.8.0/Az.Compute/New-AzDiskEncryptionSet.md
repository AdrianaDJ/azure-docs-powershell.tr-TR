---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
ms.openlocfilehash: 61d8d60925eb1d7e71ca85f92e30516d598facdf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096947"
---
# <span data-ttu-id="e6984-101">New-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="e6984-101">New-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="e6984-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6984-102">SYNOPSIS</span></span>
<span data-ttu-id="e6984-103">Disk şifreleme kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e6984-103">Creates a disk encryption set.</span></span>

## <span data-ttu-id="e6984-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e6984-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-InputObject] <PSDiskEncryptionSet>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6984-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e6984-105">DESCRIPTION</span></span>
<span data-ttu-id="e6984-106">Disk şifreleme kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e6984-106">Creates a disk encryption set.</span></span>

## <span data-ttu-id="e6984-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e6984-107">EXAMPLES</span></span>

### <span data-ttu-id="e6984-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e6984-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="e6984-109">Anahtar kasasındaki verilen etkin anahtarı kullanarak disk şifrelemesi kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e6984-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="e6984-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e6984-110">PARAMETERS</span></span>

### <span data-ttu-id="e6984-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="e6984-111">-AsJob</span></span>
<span data-ttu-id="e6984-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="e6984-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6984-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6984-113">-DefaultProfile</span></span>
<span data-ttu-id="e6984-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e6984-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6984-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6984-115">-InputObject</span></span>
<span data-ttu-id="e6984-116">Disk şifrelemesi kümesinin yerel nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e6984-116">The local object of the disk encryption set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet
Parameter Sets: (All)
Aliases: DiskEncryptionSet

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6984-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="e6984-117">-Name</span></span>
<span data-ttu-id="e6984-118">Disk şifreleme kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="e6984-118">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DiskEncryptionSetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6984-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6984-119">-ResourceGroupName</span></span>
<span data-ttu-id="e6984-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6984-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e6984-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="e6984-121">-Confirm</span></span>
<span data-ttu-id="e6984-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e6984-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6984-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6984-123">-WhatIf</span></span>
<span data-ttu-id="e6984-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e6984-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6984-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e6984-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6984-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6984-126">CommonParameters</span></span>
<span data-ttu-id="e6984-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e6984-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6984-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e6984-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6984-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e6984-129">INPUTS</span></span>

### <span data-ttu-id="e6984-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e6984-130">System.String</span></span>

### <span data-ttu-id="e6984-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDıskencryptionset</span><span class="sxs-lookup"><span data-stu-id="e6984-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="e6984-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e6984-132">OUTPUTS</span></span>

### <span data-ttu-id="e6984-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDıskencryptionset</span><span class="sxs-lookup"><span data-stu-id="e6984-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="e6984-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e6984-134">NOTES</span></span>

## <span data-ttu-id="e6984-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e6984-135">RELATED LINKS</span></span>