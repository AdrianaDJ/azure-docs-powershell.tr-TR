---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/enable-azdatalakestorekeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
ms.openlocfilehash: 0e8adfc9ef5cfd5525a0e07b35c3eb1b918b9ba7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752342"
---
# <span data-ttu-id="445f9-101">Enable-AzDataLakeStoreKeyVault</span><span class="sxs-lookup"><span data-stu-id="445f9-101">Enable-AzDataLakeStoreKeyVault</span></span>

## <span data-ttu-id="445f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="445f9-102">SYNOPSIS</span></span>
<span data-ttu-id="445f9-103">Belirtilen veri Lake Store hesabını şifrelemede Kullanıcı tarafından yönetilen Anahtar Kasası 'nı etkinleştirmeye çalışır.</span><span class="sxs-lookup"><span data-stu-id="445f9-103">Attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="445f9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="445f9-104">SYNTAX</span></span>

```
Enable-AzDataLakeStoreKeyVault [-Account] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="445f9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="445f9-105">DESCRIPTION</span></span>
<span data-ttu-id="445f9-106">**Enable-AzDataLakeStoreKeyVault** cmdlet 'i, belirtilen Data Lake Store hesabının şifrelenmesi için Kullanıcı tarafından yönetilen Anahtar Kasası etkinleştirmeye çalışır.</span><span class="sxs-lookup"><span data-stu-id="445f9-106">The **Enable-AzDataLakeStoreKeyVault** cmdlet attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="445f9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="445f9-107">EXAMPLES</span></span>

### <span data-ttu-id="445f9-108">Örnek 1: ContosoADLS hesabının Anahtar Kasası 'nı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="445f9-108">Example 1: Enable the Key Vault for the ContosoADLS account</span></span>
```
PS C:\>Enable-AzDataLakeStoreKeyVault -Name "ContosoADLS"
```

<span data-ttu-id="445f9-109">Bu komut, ContosoADLS adlı Data Lake Store hesabı için Kullanıcı tarafından yönetilen Anahtar Kasası 'nı etkinleştirmeye çalışır.</span><span class="sxs-lookup"><span data-stu-id="445f9-109">This command attempts to enable the user managed Key Vault for the Data Lake Store account named ContosoADLS.</span></span>

## <span data-ttu-id="445f9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="445f9-110">PARAMETERS</span></span>

### <span data-ttu-id="445f9-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="445f9-111">-Account</span></span>
<span data-ttu-id="445f9-112">Kullanıcı tarafından yönetilen Anahtar Kasası</span><span class="sxs-lookup"><span data-stu-id="445f9-112">The Data Lake Store account to enable the user managed Key Vault for</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="445f9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="445f9-113">-DefaultProfile</span></span>
<span data-ttu-id="445f9-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="445f9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="445f9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="445f9-115">-ResourceGroupName</span></span>
<span data-ttu-id="445f9-116">Hesapla ilişkili kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="445f9-116">Name of resource group associated with the account.</span></span> <span data-ttu-id="445f9-117">Belirtilmezse, keşfedilmesini dener.</span><span class="sxs-lookup"><span data-stu-id="445f9-117">If not specified will attempt to be discovered.</span></span>

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

### <span data-ttu-id="445f9-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="445f9-118">-Confirm</span></span>
<span data-ttu-id="445f9-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="445f9-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="445f9-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="445f9-120">-WhatIf</span></span>
<span data-ttu-id="445f9-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="445f9-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="445f9-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="445f9-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="445f9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="445f9-123">CommonParameters</span></span>
<span data-ttu-id="445f9-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="445f9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="445f9-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="445f9-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="445f9-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="445f9-126">INPUTS</span></span>

### <span data-ttu-id="445f9-127">System. String</span><span class="sxs-lookup"><span data-stu-id="445f9-127">System.String</span></span>

## <span data-ttu-id="445f9-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="445f9-128">OUTPUTS</span></span>

### <span data-ttu-id="445f9-129">System. void</span><span class="sxs-lookup"><span data-stu-id="445f9-129">System.Void</span></span>

## <span data-ttu-id="445f9-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="445f9-130">NOTES</span></span>

## <span data-ttu-id="445f9-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="445f9-131">RELATED LINKS</span></span>

[<span data-ttu-id="445f9-132">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="445f9-132">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="445f9-133">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="445f9-133">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)
