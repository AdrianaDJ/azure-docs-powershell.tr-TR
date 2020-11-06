---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: 4e252001d1459c52a35b766d34c91050df62073d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589871"
---
# <span data-ttu-id="15107-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="15107-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="15107-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15107-102">SYNOPSIS</span></span>
<span data-ttu-id="15107-103">Bir sanal makinede SQL Server Anahtar Kasası kimlik bilgileri için yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="15107-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15107-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="15107-104">SYNTAX</span></span>

```
New-AzureVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable] [-CredentialName <String>]
 [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>] [-ServicePrincipalSecret <SecureString>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15107-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="15107-105">DESCRIPTION</span></span>

## <span data-ttu-id="15107-106">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="15107-106">EXAMPLES</span></span>

## <span data-ttu-id="15107-107">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="15107-107">PARAMETERS</span></span>

### <span data-ttu-id="15107-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="15107-108">-AzureKeyVaultUrl</span></span>
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

### <span data-ttu-id="15107-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="15107-109">-CredentialName</span></span>
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

### <span data-ttu-id="15107-110">-Enable</span><span class="sxs-lookup"><span data-stu-id="15107-110">-Enable</span></span>
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

### <span data-ttu-id="15107-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15107-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="15107-112">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="15107-112">-ServicePrincipalName</span></span>
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

### <span data-ttu-id="15107-113">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="15107-113">-ServicePrincipalSecret</span></span>
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

### <span data-ttu-id="15107-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="15107-114">-Confirm</span></span>
<span data-ttu-id="15107-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="15107-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15107-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15107-116">-WhatIf</span></span>
<span data-ttu-id="15107-117">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="15107-117">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="15107-118">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="15107-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15107-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15107-119">CommonParameters</span></span>
<span data-ttu-id="15107-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="15107-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15107-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15107-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15107-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="15107-122">INPUTS</span></span>

### <span data-ttu-id="15107-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="15107-123">None</span></span>
<span data-ttu-id="15107-124">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="15107-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="15107-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="15107-125">OUTPUTS</span></span>

## <span data-ttu-id="15107-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="15107-126">NOTES</span></span>

## <span data-ttu-id="15107-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="15107-127">RELATED LINKS</span></span>

