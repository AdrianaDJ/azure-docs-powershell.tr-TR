---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: d9f732a40b61687d7970fdf24f9f9f0f841b2cc7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936953"
---
# <span data-ttu-id="9ccdf-101">New-AzVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="9ccdf-101">New-AzVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="9ccdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ccdf-102">SYNOPSIS</span></span>
<span data-ttu-id="9ccdf-103">Bir sanal makinede SQL Server Anahtar Kasası kimlik bilgileri için yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9ccdf-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

## <span data-ttu-id="9ccdf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9ccdf-104">SYNTAX</span></span>

```
New-AzVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable]
 [-CredentialName <String>] [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>]
 [-ServicePrincipalSecret <SecureString>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ccdf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9ccdf-105">DESCRIPTION</span></span>

## <span data-ttu-id="9ccdf-106">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9ccdf-106">EXAMPLES</span></span>

## <span data-ttu-id="9ccdf-107">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9ccdf-107">PARAMETERS</span></span>

### <span data-ttu-id="9ccdf-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="9ccdf-108">-AzureKeyVaultUrl</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ccdf-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="9ccdf-109">-CredentialName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ccdf-110">-Enable</span><span class="sxs-lookup"><span data-stu-id="9ccdf-110">-Enable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ccdf-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ccdf-111">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ccdf-112">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="9ccdf-112">-ServicePrincipalName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ccdf-113">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="9ccdf-113">-ServicePrincipalSecret</span></span>
```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ccdf-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="9ccdf-114">-Confirm</span></span>
<span data-ttu-id="9ccdf-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9ccdf-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ccdf-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ccdf-116">-WhatIf</span></span>
<span data-ttu-id="9ccdf-117">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9ccdf-117">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="9ccdf-118">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9ccdf-118">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ccdf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ccdf-119">CommonParameters</span></span>
<span data-ttu-id="9ccdf-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9ccdf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ccdf-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ccdf-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ccdf-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9ccdf-122">INPUTS</span></span>

### <span data-ttu-id="9ccdf-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9ccdf-123">None</span></span>
<span data-ttu-id="9ccdf-124">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="9ccdf-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9ccdf-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9ccdf-125">OUTPUTS</span></span>

### <span data-ttu-id="9ccdf-126">Microsoft. Azure. Commands. COMPUTE. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="9ccdf-126">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="9ccdf-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9ccdf-127">NOTES</span></span>

## <span data-ttu-id="9ccdf-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9ccdf-128">RELATED LINKS</span></span>

