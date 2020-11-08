---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: 50bf29524e4c16a7a7186a547505f4dcf7dac4e2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937586"
---
# <span data-ttu-id="8c604-101">New-AzVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="8c604-101">New-AzVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="8c604-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c604-102">SYNOPSIS</span></span>
<span data-ttu-id="8c604-103">Bir sanal makinede SQL Server Anahtar Kasası kimlik bilgileri için yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8c604-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

## <span data-ttu-id="8c604-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8c604-104">SYNTAX</span></span>

```
New-AzVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable] [-CredentialName <String>]
 [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>] [-ServicePrincipalSecret <SecureString>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c604-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8c604-105">DESCRIPTION</span></span>

## <span data-ttu-id="8c604-106">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8c604-106">EXAMPLES</span></span>

## <span data-ttu-id="8c604-107">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8c604-107">PARAMETERS</span></span>

### <span data-ttu-id="8c604-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="8c604-108">-AzureKeyVaultUrl</span></span>
<span data-ttu-id="8c604-109">Azure Anahtar Kasası hizmeti URL 'SI</span><span class="sxs-lookup"><span data-stu-id="8c604-109">Azure Key Vault service URL</span></span>

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

### <span data-ttu-id="8c604-110">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="8c604-110">-CredentialName</span></span>
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

### <span data-ttu-id="8c604-111">-Enable</span><span class="sxs-lookup"><span data-stu-id="8c604-111">-Enable</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c604-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c604-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="8c604-113">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="8c604-113">-ServicePrincipalName</span></span>
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

### <span data-ttu-id="8c604-114">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="8c604-114">-ServicePrincipalSecret</span></span>
```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c604-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="8c604-115">-Confirm</span></span>
<span data-ttu-id="8c604-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8c604-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c604-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c604-117">-WhatIf</span></span>
<span data-ttu-id="8c604-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8c604-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c604-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8c604-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c604-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c604-120">CommonParameters</span></span>
<span data-ttu-id="8c604-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8c604-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c604-122">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8c604-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c604-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8c604-123">INPUTS</span></span>

### <span data-ttu-id="8c604-124">System. String</span><span class="sxs-lookup"><span data-stu-id="8c604-124">System.String</span></span>

### <span data-ttu-id="8c604-125">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8c604-125">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="8c604-126">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="8c604-126">System.Security.SecureString</span></span>

## <span data-ttu-id="8c604-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8c604-127">OUTPUTS</span></span>

### <span data-ttu-id="8c604-128">Microsoft. Azure. Commands. COMPUTE. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="8c604-128">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="8c604-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8c604-129">NOTES</span></span>

## <span data-ttu-id="8c604-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8c604-130">RELATED LINKS</span></span>