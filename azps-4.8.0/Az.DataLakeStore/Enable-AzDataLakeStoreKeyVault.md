---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/enable-azdatalakestorekeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
ms.openlocfilehash: c6d15769891f02a6c1be12a277e17ca2ccba107e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107856"
---
# <span data-ttu-id="9979b-101">Enable-AzDataLakeStoreKeyVault</span><span class="sxs-lookup"><span data-stu-id="9979b-101">Enable-AzDataLakeStoreKeyVault</span></span>

## <span data-ttu-id="9979b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9979b-102">SYNOPSIS</span></span>
<span data-ttu-id="9979b-103">Belirtilen veri Lake Store hesabını şifrelemede Kullanıcı tarafından yönetilen Anahtar Kasası 'nı etkinleştirmeye çalışır.</span><span class="sxs-lookup"><span data-stu-id="9979b-103">Attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="9979b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9979b-104">SYNTAX</span></span>

```
Enable-AzDataLakeStoreKeyVault [-Account] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9979b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9979b-105">DESCRIPTION</span></span>
<span data-ttu-id="9979b-106">**Enable-AzDataLakeStoreKeyVault** cmdlet 'i, belirtilen Data Lake Store hesabının şifrelenmesi için Kullanıcı tarafından yönetilen Anahtar Kasası etkinleştirmeye çalışır.</span><span class="sxs-lookup"><span data-stu-id="9979b-106">The **Enable-AzDataLakeStoreKeyVault** cmdlet attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="9979b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9979b-107">EXAMPLES</span></span>

### <span data-ttu-id="9979b-108">Örnek 1: ContosoADLS hesabının Anahtar Kasası 'nı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="9979b-108">Example 1: Enable the Key Vault for the ContosoADLS account</span></span>
```
PS C:\>Enable-AzDataLakeStoreKeyVault -Name "ContosoADLS"
```

<span data-ttu-id="9979b-109">Bu komut, ContosoADLS adlı Data Lake Store hesabı için Kullanıcı tarafından yönetilen Anahtar Kasası 'nı etkinleştirmeye çalışır.</span><span class="sxs-lookup"><span data-stu-id="9979b-109">This command attempts to enable the user managed Key Vault for the Data Lake Store account named ContosoADLS.</span></span>

## <span data-ttu-id="9979b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9979b-110">PARAMETERS</span></span>

### <span data-ttu-id="9979b-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="9979b-111">-Account</span></span>
<span data-ttu-id="9979b-112">Kullanıcı tarafından yönetilen Anahtar Kasası</span><span class="sxs-lookup"><span data-stu-id="9979b-112">The Data Lake Store account to enable the user managed Key Vault for</span></span>

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

### <span data-ttu-id="9979b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9979b-113">-DefaultProfile</span></span>
<span data-ttu-id="9979b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9979b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9979b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9979b-115">-ResourceGroupName</span></span>
<span data-ttu-id="9979b-116">Hesapla ilişkili kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="9979b-116">Name of resource group associated with the account.</span></span> <span data-ttu-id="9979b-117">Belirtilmezse, keşfedilmesini dener.</span><span class="sxs-lookup"><span data-stu-id="9979b-117">If not specified will attempt to be discovered.</span></span>

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

### <span data-ttu-id="9979b-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="9979b-118">-Confirm</span></span>
<span data-ttu-id="9979b-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9979b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9979b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9979b-120">-WhatIf</span></span>
<span data-ttu-id="9979b-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9979b-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9979b-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9979b-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9979b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9979b-123">CommonParameters</span></span>
<span data-ttu-id="9979b-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9979b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9979b-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9979b-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9979b-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9979b-126">INPUTS</span></span>

### <span data-ttu-id="9979b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="9979b-127">System.String</span></span>

## <span data-ttu-id="9979b-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9979b-128">OUTPUTS</span></span>

### <span data-ttu-id="9979b-129">System. void</span><span class="sxs-lookup"><span data-stu-id="9979b-129">System.Void</span></span>

## <span data-ttu-id="9979b-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9979b-130">NOTES</span></span>

## <span data-ttu-id="9979b-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9979b-131">RELATED LINKS</span></span>

[<span data-ttu-id="9979b-132">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9979b-132">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="9979b-133">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="9979b-133">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

