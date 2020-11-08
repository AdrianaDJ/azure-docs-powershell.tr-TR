---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azmanagedhsmroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmRoleDefinition.md
ms.openlocfilehash: 60ba6fbf57fa9e1ac9e25a913fb9755902b56ddd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275307"
---
# <span data-ttu-id="6bdbd-101">Get-AzManagedHsmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="6bdbd-101">Get-AzManagedHsmRoleDefinition</span></span>

## <span data-ttu-id="6bdbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bdbd-102">SYNOPSIS</span></span>
<span data-ttu-id="6bdbd-103">Verilen kapsamda verilen bir yönetilen HSM 'nin rol tanımlarını listeler.</span><span class="sxs-lookup"><span data-stu-id="6bdbd-103">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="6bdbd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6bdbd-104">SYNTAX</span></span>

### <span data-ttu-id="6bdbd-105">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6bdbd-105">Interactive (Default)</span></span>
```
Get-AzManagedHsmRoleDefinition [-HsmName] <String> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6bdbd-106">ByName</span><span class="sxs-lookup"><span data-stu-id="6bdbd-106">ByName</span></span>
```
Get-AzManagedHsmRoleDefinition [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6bdbd-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6bdbd-107">DESCRIPTION</span></span>
<span data-ttu-id="6bdbd-108">Verilen kapsamda verilen bir yönetilen HSM 'nin rol tanımlarını listeler.</span><span class="sxs-lookup"><span data-stu-id="6bdbd-108">List role definitions of a given managed HSM at a given scope.</span></span>

## <span data-ttu-id="6bdbd-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6bdbd-109">EXAMPLES</span></span>

### <span data-ttu-id="6bdbd-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6bdbd-110">Example 1</span></span>
```powershell
PS C:\> Get-AzManagedHsmRoleDefinition -HsmName myHsm -Scope "/keys"

RoleName                              Description Permissions
--------                              ----------- -----------
Managed HSM Administrator                         1 permission(s)
Managed HSM Crypto Officer                        1 permission(s)
Managed HSM Crypto User                           1 permission(s)
Managed HSM Policy Administrator                  1 permission(s)
Managed HSM Crypto Auditor                        1 permission(s)
Managed HSM Crypto Service Encryption             1 permission(s)
Managed HSM Backup                                1 permission(s)
```

<span data-ttu-id="6bdbd-111">Örnekte, "/Keys" kapsamındaki tüm roller listelenir.</span><span class="sxs-lookup"><span data-stu-id="6bdbd-111">The example lists all the roles at "/keys" scope.</span></span>

### <span data-ttu-id="6bdbd-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="6bdbd-112">Example 2</span></span>
```powershell
PS C:\> $backupRole = Get-AzManagedHsmRoleDefinition -HsmName myHsm -RoleDefinitionName "managed hsm backup"

PS C:\> $backupRole.Permissions

AllowedActions DeniedActions AllowedDataActions DeniedDataActions
-------------- ------------- ------------------ -----------------
0 action(s)    0 action(s)   3 action(s)        0 action(s)

PS C:\> $backupRole.Permissions.AllowedDataActions

Microsoft.KeyVault/managedHsm/backup/start/action
Microsoft.KeyVault/managedHsm/backup/status/action
Microsoft.KeyVault/managedHsm/keys/backup/action

RoleName                              Description Permissions
--------                              ----------- -----------
Managed HSM Administrator                         1 permission(s)
Managed HSM Crypto Officer                        1 permission(s)
Managed HSM Crypto User                           1 permission(s)
Managed HSM Policy Administrator                  1 permission(s)
Managed HSM Crypto Auditor                        1 permission(s)
Managed HSM Crypto Service Encryption             1 permission(s)
Managed HSM Backup                                1 permission(s)
```

<span data-ttu-id="6bdbd-113">Örnek "Managed HSM Backup" rolünü alır ve izinlerini inceler.</span><span class="sxs-lookup"><span data-stu-id="6bdbd-113">The example gets the "Managed HSM Backup" role and inspects its permissions.</span></span>

## <span data-ttu-id="6bdbd-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6bdbd-114">PARAMETERS</span></span>

### <span data-ttu-id="6bdbd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bdbd-115">-DefaultProfile</span></span>
<span data-ttu-id="6bdbd-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6bdbd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bdbd-117">-HsmName</span><span class="sxs-lookup"><span data-stu-id="6bdbd-117">-HsmName</span></span>
<span data-ttu-id="6bdbd-118">HSM adı.</span><span class="sxs-lookup"><span data-stu-id="6bdbd-118">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bdbd-119">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="6bdbd-119">-RoleDefinitionName</span></span>
<span data-ttu-id="6bdbd-120">Alınacak rol tanımının adı.</span><span class="sxs-lookup"><span data-stu-id="6bdbd-120">Name of the role definition to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: RoleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bdbd-121">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="6bdbd-121">-Scope</span></span>
<span data-ttu-id="6bdbd-122">Rol atamasının veya tanımının uygulandığı kapsam; Örneğin, '/' veya '/Keys ' veya '/keys/{keyName} '.</span><span class="sxs-lookup"><span data-stu-id="6bdbd-122">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="6bdbd-123">'/' gözardı edildiğinde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6bdbd-123">'/' is used when omitted.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bdbd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bdbd-124">CommonParameters</span></span>
<span data-ttu-id="6bdbd-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6bdbd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bdbd-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6bdbd-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bdbd-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6bdbd-127">INPUTS</span></span>

### <span data-ttu-id="6bdbd-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6bdbd-128">None</span></span>

## <span data-ttu-id="6bdbd-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6bdbd-129">OUTPUTS</span></span>

### <span data-ttu-id="6bdbd-130">Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="6bdbd-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleDefinition</span></span>

## <span data-ttu-id="6bdbd-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6bdbd-131">NOTES</span></span>

## <span data-ttu-id="6bdbd-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6bdbd-132">RELATED LINKS</span></span>
