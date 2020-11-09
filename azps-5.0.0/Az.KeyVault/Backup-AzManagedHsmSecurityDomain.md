---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azmanagedhsmsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmSecurityDomain.md
ms.openlocfilehash: 10a54afa8a6ef2e37beebd9d6cdcd304b2d13979
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319914"
---
# <span data-ttu-id="5ff73-101">Backup-AzManagedHsmSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="5ff73-101">Backup-AzManagedHsmSecurityDomain</span></span>

## <span data-ttu-id="5ff73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ff73-102">SYNOPSIS</span></span>
<span data-ttu-id="5ff73-103">Yönetilen bir HSM 'in güvenlik etki alanı verilerini geri yükleme için yedekler.</span><span class="sxs-lookup"><span data-stu-id="5ff73-103">Backs up the security domain data of a managed HSM for restoring.</span></span>

## <span data-ttu-id="5ff73-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5ff73-104">SYNTAX</span></span>

### <span data-ttu-id="5ff73-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5ff73-105">ByName (Default)</span></span>
```
Backup-AzManagedHsmSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ff73-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5ff73-106">ByInputObject</span></span>
```
Backup-AzManagedHsmSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ff73-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5ff73-107">DESCRIPTION</span></span>
<span data-ttu-id="5ff73-108">Bu cmdlet, geri yüklemek için yönetilen bir HSM 'in güvenlik etki alanı verilerini yedekler.</span><span class="sxs-lookup"><span data-stu-id="5ff73-108">This cmdlet backs up the security domain data of a managed HSM for restoring.</span></span>

## <span data-ttu-id="5ff73-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5ff73-109">EXAMPLES</span></span>

### <span data-ttu-id="5ff73-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5ff73-110">Example 1</span></span>
```powershell
PS C:\Users\username\> Backup-AzManagedHsmSecurityDomain -Name testmhsm -Certificates {pathOfCertificates}/sd1.cer, {pathOfCertificates}/sd2.cer, {pathOfCertificates}/sd3.cer -OutputPath {pathOfOutput}/sd.ps.json -Quorum 2
```

<span data-ttu-id="5ff73-111">Bu komut testmhsm adlı yönetilen HSM 'yi alır ve belirtilen çıktı dosyasına bu yönetilen HSM güvenlik etki alanının yedeğini kaydeder.</span><span class="sxs-lookup"><span data-stu-id="5ff73-111">This command retrieves the managed HSM named testmhsm and saves a backup of that managed HSM security domain to the specified output file.</span></span>

## <span data-ttu-id="5ff73-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5ff73-112">PARAMETERS</span></span>

### <span data-ttu-id="5ff73-113">-Sertifikalar</span><span class="sxs-lookup"><span data-stu-id="5ff73-113">-Certificates</span></span>
<span data-ttu-id="5ff73-114">Güvenlik etki alanı verilerini şifrelemek için kullanılan sertifikaların yolları.</span><span class="sxs-lookup"><span data-stu-id="5ff73-114">Paths to the certificates that are used to encrypt the security domain data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ff73-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ff73-115">-DefaultProfile</span></span>
<span data-ttu-id="5ff73-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5ff73-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ff73-117">-Force</span><span class="sxs-lookup"><span data-stu-id="5ff73-117">-Force</span></span>
<span data-ttu-id="5ff73-118">Var olan dosyanın üzerine yazılıp yazılmayacağını belirtin.</span><span class="sxs-lookup"><span data-stu-id="5ff73-118">Specify whether to overwrite existing file.</span></span>

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

### <span data-ttu-id="5ff73-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ff73-119">-InputObject</span></span>
<span data-ttu-id="5ff73-120">Yönetilen HSM 'yi temsil eden nesne.</span><span class="sxs-lookup"><span data-stu-id="5ff73-120">Object representing a managed HSM.</span></span>

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

### <span data-ttu-id="5ff73-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="5ff73-121">-Name</span></span>
<span data-ttu-id="5ff73-122">Yönetilen HSM adı.</span><span class="sxs-lookup"><span data-stu-id="5ff73-122">Name of the managed HSM.</span></span>

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

### <span data-ttu-id="5ff73-123">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="5ff73-123">-OutputPath</span></span>
<span data-ttu-id="5ff73-124">Güvenlik etki alanı verilerinin indirileceği yolu belirtin.</span><span class="sxs-lookup"><span data-stu-id="5ff73-124">Specify the path where security domain data will be downloaded to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ff73-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="5ff73-125">-PassThru</span></span>
<span data-ttu-id="5ff73-126">Belirtildiğinde, cmdlet başarılı olduğunda Boole değeri döndürülür.</span><span class="sxs-lookup"><span data-stu-id="5ff73-126">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="5ff73-127">-Çekirdek</span><span class="sxs-lookup"><span data-stu-id="5ff73-127">-Quorum</span></span>
<span data-ttu-id="5ff73-128">Kurtarma için güvenlik etki alanının şifresini çözmek için gereken en az paylaşım sayısı.</span><span class="sxs-lookup"><span data-stu-id="5ff73-128">The minimum number of shares required to decrypt the security domain for recovery.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ff73-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="5ff73-129">-Confirm</span></span>
<span data-ttu-id="5ff73-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5ff73-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ff73-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ff73-131">-WhatIf</span></span>
<span data-ttu-id="5ff73-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5ff73-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ff73-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5ff73-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ff73-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ff73-134">CommonParameters</span></span>
<span data-ttu-id="5ff73-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5ff73-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ff73-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5ff73-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ff73-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5ff73-137">INPUTS</span></span>

### <span data-ttu-id="5ff73-138">Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultidentityıtem</span><span class="sxs-lookup"><span data-stu-id="5ff73-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="5ff73-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5ff73-139">OUTPUTS</span></span>

### <span data-ttu-id="5ff73-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5ff73-140">System.Boolean</span></span>

## <span data-ttu-id="5ff73-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5ff73-141">NOTES</span></span>

## <span data-ttu-id="5ff73-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5ff73-142">RELATED LINKS</span></span>
