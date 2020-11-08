---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SqlVirtualMachine.dll-Help.xml
Module Name: Az.SqlVirtualMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.sqlvirtualmachine/new-azsqlvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SqlVirtualMachine/SqlVirtualMachine/help/New-AzSqlVMConfig.md
ms.openlocfilehash: 0f914ab2f5c39cd53239302b2f0acd12a3e13133
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937957"
---
# <span data-ttu-id="32b2b-101">New-AzSqlVMConfig</span><span class="sxs-lookup"><span data-stu-id="32b2b-101">New-AzSqlVMConfig</span></span>

## <span data-ttu-id="32b2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32b2b-102">SYNOPSIS</span></span>
<span data-ttu-id="32b2b-103">SQL sanal makinesi için yeni bir yapılandırma oluşturur.</span><span class="sxs-lookup"><span data-stu-id="32b2b-103">Creates a new configuration for a sql virtual machine.</span></span>

## <span data-ttu-id="32b2b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="32b2b-104">SYNTAX</span></span>

```
New-AzSqlVMConfig [-LicenseType] <String> [-Offer <String>] [-Sku <String>] [-SqlManagementType <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32b2b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="32b2b-105">DESCRIPTION</span></span>
<span data-ttu-id="32b2b-106">New-AzSqlVMConfig cmdlet 'i SQL sanal makinesi için yeni bir yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="32b2b-106">The New-AzSqlVMConfig cmdlet creates a new configuration object for a sql virtual machine.</span></span>

## <span data-ttu-id="32b2b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="32b2b-107">EXAMPLES</span></span>

### <span data-ttu-id="32b2b-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="32b2b-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzSqlVMConfig -LicenseType "PAYG"
PS C:\> New-AzSqlVM -ResourceGroupName "ResourceGroup01" -Name "vm" -SqlVM $config
Name ResourceGroupName  LicenseType Sku       Offer          SqlManagementType
---- -----------------  ----------- ---       -----          -----------------
vm   ResourceGroup01    PAYG        Developer SQL2017-WS2016 Full
```

<span data-ttu-id="32b2b-109">Azure SQL sanal makinesini oluşturmak için kullanılabilen, SQL sanal makinesinin yerel yapılandırılabilir bir nesnesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="32b2b-109">Creates a local configurable object of sql virtual machine that can be used in order to create an Azure sql virtual machine.</span></span>

## <span data-ttu-id="32b2b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="32b2b-110">PARAMETERS</span></span>

### <span data-ttu-id="32b2b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32b2b-111">-DefaultProfile</span></span>
<span data-ttu-id="32b2b-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="32b2b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32b2b-113">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="32b2b-113">-LicenseType</span></span>
<span data-ttu-id="32b2b-114">SQL sanal makine lisans türü.</span><span class="sxs-lookup"><span data-stu-id="32b2b-114">SQL virtual machine license type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b2b-115">-Teklif</span><span class="sxs-lookup"><span data-stu-id="32b2b-115">-Offer</span></span>
<span data-ttu-id="32b2b-116">SQL sanal makinesi teklifi.</span><span class="sxs-lookup"><span data-stu-id="32b2b-116">SQL virtual machine offer.</span></span>

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

### <span data-ttu-id="32b2b-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="32b2b-117">-Sku</span></span>
<span data-ttu-id="32b2b-118">SQL sanal makinesi sürümü türü.</span><span class="sxs-lookup"><span data-stu-id="32b2b-118">SQL virtual machine edition type.</span></span>

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

### <span data-ttu-id="32b2b-119">-SqlManagementType</span><span class="sxs-lookup"><span data-stu-id="32b2b-119">-SqlManagementType</span></span>
<span data-ttu-id="32b2b-120">SQL sanal makine yönetimi türü.</span><span class="sxs-lookup"><span data-stu-id="32b2b-120">SQL virtual machine management type.</span></span>

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

### <span data-ttu-id="32b2b-121">Etiketli</span><span class="sxs-lookup"><span data-stu-id="32b2b-121">-Tag</span></span>
<span data-ttu-id="32b2b-122">SQL sanal makinesiyle ilişkilendirilecek Etiketler</span><span class="sxs-lookup"><span data-stu-id="32b2b-122">The tags to associate with the SQL virtual machine</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b2b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32b2b-123">CommonParameters</span></span>
<span data-ttu-id="32b2b-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="32b2b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32b2b-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="32b2b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32b2b-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="32b2b-126">INPUTS</span></span>

### <span data-ttu-id="32b2b-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="32b2b-127">None</span></span>

## <span data-ttu-id="32b2b-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="32b2b-128">OUTPUTS</span></span>

### <span data-ttu-id="32b2b-129">Microsoft. Azure. Commands. SqlVirtualMachine. SqlVirtualMachine. model. azures, Vmmodel</span><span class="sxs-lookup"><span data-stu-id="32b2b-129">Microsoft.Azure.Commands.SqlVirtualMachine.SqlVirtualMachine.Model.AzureSqlVMModel</span></span>

## <span data-ttu-id="32b2b-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="32b2b-130">NOTES</span></span>

## <span data-ttu-id="32b2b-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="32b2b-131">RELATED LINKS</span></span>