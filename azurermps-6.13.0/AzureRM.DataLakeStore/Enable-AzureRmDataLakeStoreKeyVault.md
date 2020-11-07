---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/enable-azurermdatalakestorekeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Enable-AzureRmDataLakeStoreKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Enable-AzureRmDataLakeStoreKeyVault.md
ms.openlocfilehash: 5316a55e29acb8edc5bd102d118eb2bcc53c2c30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591986"
---
# <span data-ttu-id="3060e-101">Enable-AzureRmDataLakeStoreKeyVault</span><span class="sxs-lookup"><span data-stu-id="3060e-101">Enable-AzureRmDataLakeStoreKeyVault</span></span>

## <span data-ttu-id="3060e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3060e-102">SYNOPSIS</span></span>
<span data-ttu-id="3060e-103">Belirtilen veri Lake Store hesabını şifrelemede Kullanıcı tarafından yönetilen Anahtar Kasası 'nı etkinleştirmeye çalışır.</span><span class="sxs-lookup"><span data-stu-id="3060e-103">Attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3060e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3060e-104">SYNTAX</span></span>

```
Enable-AzureRmDataLakeStoreKeyVault [-Account] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3060e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3060e-105">DESCRIPTION</span></span>
<span data-ttu-id="3060e-106">**Enable-AzureRmDataLakeStoreKeyVault** cmdlet 'i, belirtilen Data Lake Store hesabının şifrelenmesi için Kullanıcı tarafından yönetilen Anahtar Kasası etkinleştirmeye çalışır.</span><span class="sxs-lookup"><span data-stu-id="3060e-106">The **Enable-AzureRmDataLakeStoreKeyVault** cmdlet attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="3060e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3060e-107">EXAMPLES</span></span>

### <span data-ttu-id="3060e-108">Örnek 1: ContosoADLS hesabının Anahtar Kasası 'nı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="3060e-108">Example 1: Enable the Key Vault for the ContosoADLS account</span></span>
```
PS C:\>Enable-AzureRmDataLakeStoreKeyVault -Name "ContosoADLS"
```

<span data-ttu-id="3060e-109">Bu komut, ContosoADLS adlı Data Lake Store hesabı için Kullanıcı tarafından yönetilen Anahtar Kasası 'nı etkinleştirmeye çalışır.</span><span class="sxs-lookup"><span data-stu-id="3060e-109">This command attempts to enable the user managed Key Vault for the Data Lake Store account named ContosoADLS.</span></span>

## <span data-ttu-id="3060e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3060e-110">PARAMETERS</span></span>

### <span data-ttu-id="3060e-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="3060e-111">-Account</span></span>
<span data-ttu-id="3060e-112">Kullanıcı tarafından yönetilen Anahtar Kasası</span><span class="sxs-lookup"><span data-stu-id="3060e-112">The Data Lake Store account to enable the user managed Key Vault for</span></span>

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

### <span data-ttu-id="3060e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3060e-113">-DefaultProfile</span></span>
<span data-ttu-id="3060e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3060e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3060e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3060e-115">-ResourceGroupName</span></span>
<span data-ttu-id="3060e-116">Hesapla ilişkili kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="3060e-116">Name of resource group associated with the account.</span></span> <span data-ttu-id="3060e-117">Belirtilmezse, keşfedilmesini dener.</span><span class="sxs-lookup"><span data-stu-id="3060e-117">If not specified will attempt to be discovered.</span></span>

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

### <span data-ttu-id="3060e-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="3060e-118">-Confirm</span></span>
<span data-ttu-id="3060e-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3060e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3060e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3060e-120">-WhatIf</span></span>
<span data-ttu-id="3060e-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3060e-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3060e-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3060e-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3060e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3060e-123">CommonParameters</span></span>
<span data-ttu-id="3060e-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3060e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3060e-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3060e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3060e-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3060e-126">INPUTS</span></span>

### <span data-ttu-id="3060e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="3060e-127">System.String</span></span>

## <span data-ttu-id="3060e-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3060e-128">OUTPUTS</span></span>

### <span data-ttu-id="3060e-129">System. void</span><span class="sxs-lookup"><span data-stu-id="3060e-129">System.Void</span></span>

## <span data-ttu-id="3060e-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3060e-130">NOTES</span></span>

## <span data-ttu-id="3060e-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3060e-131">RELATED LINKS</span></span>

[<span data-ttu-id="3060e-132">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3060e-132">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="3060e-133">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3060e-133">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)
