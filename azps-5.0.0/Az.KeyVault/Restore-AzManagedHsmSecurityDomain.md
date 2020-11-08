---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azmanagedhsmsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsmSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsmSecurityDomain.md
ms.openlocfilehash: f743b408917e575005589598a49fafbd8cc95379
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280195"
---
# <span data-ttu-id="3daa5-101">Restore-AzManagedHsmSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="3daa5-101">Restore-AzManagedHsmSecurityDomain</span></span>

## <span data-ttu-id="3daa5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3daa5-102">SYNOPSIS</span></span>
<span data-ttu-id="3daa5-103">Önceki yedeklenen güvenlik etki alanı verilerini yönetilen bir HSM 'ye geri yükler.</span><span class="sxs-lookup"><span data-stu-id="3daa5-103">Restores previous backed up security domain data to a managed HSM.</span></span>

## <span data-ttu-id="3daa5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3daa5-104">SYNTAX</span></span>

### <span data-ttu-id="3daa5-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3daa5-105">ByName (Default)</span></span>
```
Restore-AzManagedHsmSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3daa5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3daa5-106">ByInputObject</span></span>
```
Restore-AzManagedHsmSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru]
 -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3daa5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3daa5-107">DESCRIPTION</span></span>
<span data-ttu-id="3daa5-108">Bu cmdlet, önceki yedeklenen güvenlik etki alanı verilerini yönetilen bir HSM 'ye geri yükler.</span><span class="sxs-lookup"><span data-stu-id="3daa5-108">This cmdlet restores previous backed up security domain data to a managed HSM.</span></span>

## <span data-ttu-id="3daa5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3daa5-109">EXAMPLES</span></span>

### <span data-ttu-id="3daa5-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3daa5-110">Example 1</span></span>
```powershell
PS C:\> $keys = @{PublicKey = "sd1.cer"; PrivateKey = "sd1.key"}, @{PublicKey = "sd2.cer"; PrivateKey = "sd2.key"}, @{PublicKey = "sd3.cer"; PrivateKey = "sd3.key"}
PS C:\> Restore-AzManagedHsmSecurityDomain -Name testmhsm -Keys $keys -SecurityDomainPath {pathOfBackup}\sd.ps.json
```

<span data-ttu-id="3daa5-111">İlk olarak, güvenlik etki alanı verilerinin şifresini çözmek için anahtarların sağlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="3daa5-111">First, the keys need be provided to decrypt the security domain data.</span></span> <span data-ttu-id="3daa5-112">Ardından **restore-AzManagedHsmSecurityDomain** komutu, önceki yedeklenen güvenlik etki alanı verilerini YÖNETILEN bir HSM 'ye bu tuşları kullanarak geri yükler.</span><span class="sxs-lookup"><span data-stu-id="3daa5-112">Then, The **Restore-AzManagedHsmSecurityDomain** command restores previous backed up security domain data to a managed HSM using these keys.</span></span>

## <span data-ttu-id="3daa5-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3daa5-113">PARAMETERS</span></span>

### <span data-ttu-id="3daa5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3daa5-114">-DefaultProfile</span></span>
<span data-ttu-id="3daa5-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3daa5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3daa5-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3daa5-116">-InputObject</span></span>
<span data-ttu-id="3daa5-117">Yönetilen HSM 'yi temsil eden nesne.</span><span class="sxs-lookup"><span data-stu-id="3daa5-117">Object representing a managed HSM.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3daa5-118">Tuşları</span><span class="sxs-lookup"><span data-stu-id="3daa5-118">-Keys</span></span>
<span data-ttu-id="3daa5-119">Güvenlik etki alanı verilerinin şifresini çözmek için kullanılan anahtarlarla ilgili bilgiler.</span><span class="sxs-lookup"><span data-stu-id="3daa5-119">Information about the keys that are used to decrypt the security domain data.</span></span>
<span data-ttu-id="3daa5-120">Nasıl oluşturulduğunu görün.</span><span class="sxs-lookup"><span data-stu-id="3daa5-120">See examples for how it is constructed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.SecurityDomain.Models.KeyPath[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3daa5-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="3daa5-121">-Name</span></span>
<span data-ttu-id="3daa5-122">Yönetilen HSM adı.</span><span class="sxs-lookup"><span data-stu-id="3daa5-122">Name of the managed HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: HsmName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3daa5-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3daa5-123">-PassThru</span></span>
<span data-ttu-id="3daa5-124">Belirtildiğinde, cmdlet başarılı olduğunda Boole değeri döndürülür.</span><span class="sxs-lookup"><span data-stu-id="3daa5-124">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="3daa5-125">-SecurityDomainPath</span><span class="sxs-lookup"><span data-stu-id="3daa5-125">-SecurityDomainPath</span></span>
<span data-ttu-id="3daa5-126">Şifreli güvenlik etki alanı verilerinin yolunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="3daa5-126">Specify the path to the encrypted security domain data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3daa5-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="3daa5-127">-Confirm</span></span>
<span data-ttu-id="3daa5-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3daa5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3daa5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3daa5-129">-WhatIf</span></span>
<span data-ttu-id="3daa5-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3daa5-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3daa5-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3daa5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3daa5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3daa5-132">CommonParameters</span></span>
<span data-ttu-id="3daa5-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3daa5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3daa5-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3daa5-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3daa5-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3daa5-135">INPUTS</span></span>

### <span data-ttu-id="3daa5-136">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultidentityıtem</span><span class="sxs-lookup"><span data-stu-id="3daa5-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="3daa5-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3daa5-137">OUTPUTS</span></span>

### <span data-ttu-id="3daa5-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3daa5-138">System.Boolean</span></span>

## <span data-ttu-id="3daa5-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3daa5-139">NOTES</span></span>

## <span data-ttu-id="3daa5-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3daa5-140">RELATED LINKS</span></span>
