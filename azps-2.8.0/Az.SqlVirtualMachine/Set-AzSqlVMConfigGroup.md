---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/set-azsqlvmconfiggroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/Set-AzSqlVMConfigGroup.md
ms.openlocfilehash: a2615f5d016d16edb1201e88c31a8be62771ae59
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933962"
---
# <span data-ttu-id="33d77-101">Set-AzSqlVMConfigGroup</span><span class="sxs-lookup"><span data-stu-id="33d77-101">Set-AzSqlVMConfigGroup</span></span>

## <span data-ttu-id="33d77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33d77-102">SYNOPSIS</span></span>
<span data-ttu-id="33d77-103">SQL sanal makine yapılandırmasındaki bir SQL sanal makine grubuyla ilgili bilgileri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="33d77-103">Set the information relative to a sql virtual machine group in a sql virtual machine configuration.</span></span>

## <span data-ttu-id="33d77-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="33d77-104">SYNTAX</span></span>

```
Set-AzSqlVMConfigGroup [-SqlVM] <AzureSqlVMModel> [-SqlVMGroup] <AzureSqlVMGroupModel>
 -ClusterOperatorAccountPassword <SecureString> -SqlServiceAccountPassword <SecureString>
 [-ClusterBootstrapAccountPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="33d77-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="33d77-105">DESCRIPTION</span></span>
<span data-ttu-id="33d77-106">Set-AzSqlVMConfigGroup cmdlet, SQL sanal makine yapılandırması için SQL sanal makine grubuna katılmak amacıyla gereken bilgileri ayarladı.</span><span class="sxs-lookup"><span data-stu-id="33d77-106">The Set-AzSqlVMConfigGroup cmdlet set the information needed in order to join a sql virtual machine group for a sql virtual machine configuration.</span></span>

## <span data-ttu-id="33d77-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="33d77-107">EXAMPLES</span></span>

### <span data-ttu-id="33d77-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="33d77-108">Example 1</span></span>
```powershell
PS C:\> $config = Set-AzSqlVMConfigGroup -SqlVM $config -SqlVMGroup $group -ClusterOperatorAccountPassword 'password' -SqlServiceAccountPassword 'password'
```

<span data-ttu-id="33d77-109">SQL sanal makine yapılandırmasının grup listesini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="33d77-109">Update the group informations of a sql virtual machine configuration.</span></span>

## <span data-ttu-id="33d77-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="33d77-110">PARAMETERS</span></span>

### <span data-ttu-id="33d77-111">-ClusterBootstrapAccountPassword</span><span class="sxs-lookup"><span data-stu-id="33d77-111">-ClusterBootstrapAccountPassword</span></span>
<span data-ttu-id="33d77-112">Küme önyükleme hesabının parolası</span><span class="sxs-lookup"><span data-stu-id="33d77-112">Password for the cluster bootstrap account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33d77-113">-ClusterOperatorAccountPassword</span><span class="sxs-lookup"><span data-stu-id="33d77-113">-ClusterOperatorAccountPassword</span></span>
<span data-ttu-id="33d77-114">Küme işletmeni hesabının parolası</span><span class="sxs-lookup"><span data-stu-id="33d77-114">Password for the cluster operator account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33d77-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33d77-115">-DefaultProfile</span></span>
<span data-ttu-id="33d77-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="33d77-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33d77-117">-SqlServiceAccountPassword</span><span class="sxs-lookup"><span data-stu-id="33d77-117">-SqlServiceAccountPassword</span></span>
<span data-ttu-id="33d77-118">SQL hizmeti hesabının parolası</span><span class="sxs-lookup"><span data-stu-id="33d77-118">Password for the SQL service account</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33d77-119">-SqlVM</span><span class="sxs-lookup"><span data-stu-id="33d77-119">-SqlVM</span></span>
<span data-ttu-id="33d77-120">SQL sanal makine yapılandırması</span><span class="sxs-lookup"><span data-stu-id="33d77-120">The SQL virtual machine configuration which group membership will be added to</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33d77-121">-SqlVMGroup</span><span class="sxs-lookup"><span data-stu-id="33d77-121">-SqlVMGroup</span></span>
<span data-ttu-id="33d77-122">SQL sanal makinesinin bir parçası olacak Grup</span><span class="sxs-lookup"><span data-stu-id="33d77-122">The group the SQL virtual machine will be part of</span></span>

```yaml
Type: Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMGroupModel
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33d77-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33d77-123">CommonParameters</span></span>
<span data-ttu-id="33d77-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="33d77-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33d77-125">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="33d77-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33d77-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="33d77-126">INPUTS</span></span>

### <span data-ttu-id="33d77-127">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. azures, Vmmodel</span><span class="sxs-lookup"><span data-stu-id="33d77-127">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="33d77-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="33d77-128">OUTPUTS</span></span>

### <span data-ttu-id="33d77-129">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. azures, Vmmodel</span><span class="sxs-lookup"><span data-stu-id="33d77-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="33d77-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="33d77-130">NOTES</span></span>

## <span data-ttu-id="33d77-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="33d77-131">RELATED LINKS</span></span>
