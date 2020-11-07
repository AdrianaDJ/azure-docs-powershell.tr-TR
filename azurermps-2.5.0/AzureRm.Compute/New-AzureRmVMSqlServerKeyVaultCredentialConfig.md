---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
ms.openlocfilehash: ee627065d1d6be8037d1a9b054ec6452b9becb41
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939784"
---
# <span data-ttu-id="ea1d6-101">New-AzureRmVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="ea1d6-101">New-AzureRmVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="ea1d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea1d6-102">SYNOPSIS</span></span>
<span data-ttu-id="ea1d6-103">Bir sanal makinede SQL Server Anahtar Kasası kimlik bilgileri için yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ea1d6-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea1d6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ea1d6-104">SYNTAX</span></span>

```
New-AzureRmVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable]
 [-CredentialName <String>] [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>]
 [-ServicePrincipalSecret <SecureString>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea1d6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ea1d6-105">DESCRIPTION</span></span>

## <span data-ttu-id="ea1d6-106">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ea1d6-106">EXAMPLES</span></span>

## <span data-ttu-id="ea1d6-107">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ea1d6-107">PARAMETERS</span></span>

### <span data-ttu-id="ea1d6-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="ea1d6-108">-AzureKeyVaultUrl</span></span>
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

### <span data-ttu-id="ea1d6-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="ea1d6-109">-CredentialName</span></span>
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

### <span data-ttu-id="ea1d6-110">-Enable</span><span class="sxs-lookup"><span data-stu-id="ea1d6-110">-Enable</span></span>
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

### <span data-ttu-id="ea1d6-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea1d6-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="ea1d6-112">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="ea1d6-112">-ServicePrincipalName</span></span>
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

### <span data-ttu-id="ea1d6-113">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="ea1d6-113">-ServicePrincipalSecret</span></span>
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

### <span data-ttu-id="ea1d6-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="ea1d6-114">-Confirm</span></span>
<span data-ttu-id="ea1d6-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ea1d6-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea1d6-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea1d6-116">-WhatIf</span></span>
<span data-ttu-id="ea1d6-117">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ea1d6-117">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="ea1d6-118">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ea1d6-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea1d6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea1d6-119">CommonParameters</span></span>
<span data-ttu-id="ea1d6-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ea1d6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea1d6-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea1d6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea1d6-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ea1d6-122">INPUTS</span></span>

### <span data-ttu-id="ea1d6-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ea1d6-123">None</span></span>
<span data-ttu-id="ea1d6-124">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="ea1d6-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ea1d6-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ea1d6-125">OUTPUTS</span></span>

### <span data-ttu-id="ea1d6-126">Microsoft. Azure. Commands. COMPUTE. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="ea1d6-126">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="ea1d6-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ea1d6-127">NOTES</span></span>

## <span data-ttu-id="ea1d6-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ea1d6-128">RELATED LINKS</span></span>

